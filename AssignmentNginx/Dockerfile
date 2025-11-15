# Nginx image
FROM nginx:latest

# Remove default Nginx website
RUN rm -rf /usr/share/nginx/html/index.html

# Working directory
WORKDIR /usr/share/nginx/html

# Copy your website files to the Nginx web root
COPY ./web/index.html /usr/share/nginx/html

# Expose HTTP port
EXPOSE 80

# Start Nginx
CMD ["nginx", "-g", "daemon off;"]