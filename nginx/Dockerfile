FROM nginx:latest

# Set the working directory
WORKDIR /etc/nginx

# Copy Nginx configuration files
ADD nginx.conf nginx.conf
ADD conf.d/default.conf conf.d/default.conf

COPY index.html /usr/share/nginx/html

# Expose ports
EXPOSE 80

# Install curl for health checks
RUN apt-get update && \
apt-get install -y curl && \
rm -rf /var/lib/apt/lists/*

# Set environment variables
ENV BACKEND_SERVERS="backend1.example.com backend2.example.com"

# Start Nginx
CMD ["nginx", "-g", "daemon off;"]