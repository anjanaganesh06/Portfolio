FROM nginx:alpine

# Set working directory
WORKDIR /usr/share/nginx/html

# Remove existing files in the directory
RUN rm -rf ./*

# Install git
RUN apk add --no-cache git

# Clone the repository into a temporary folder
RUN git clone https://github.com/anjanaganesh06/Portfolio.git /temp-repo && \
    cp -r /temp-repo/* . && \
    rm -rf /temp-repo

# Expose port 80 for the web server
EXPOSE 80

# Start nginx
CMD ["nginx", "-g", "daemon off;"]
