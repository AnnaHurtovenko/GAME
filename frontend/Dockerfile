# 1. Using the basic Nginx image
FROM nginx:alpine

# 2. Setting up a working directory for the frontend
WORKDIR /usr/share/nginx/html

# 3. Delete standard Nginx files
RUN rm -rf ./*

# 4. Copy static files to a container
COPY . .

# 5. Port listening to Nginx
EXPOSE 80

# 6. Define the start command
CMD ["nginx", "-g", "daemon off;"]
