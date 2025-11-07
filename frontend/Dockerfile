# 1️⃣ Use Node for build stage
FROM node:18 AS build

WORKDIR /app
COPY package*.json ./
RUN npm install

# 2️⃣ Build frontend
COPY . .
RUN npm run build

# 3️⃣ Use Nginx to serve static files
FROM nginx:stable-alpine

# 4️⃣ Copy build output to Nginx html folder
COPY --from=build /app/dist /usr/share/nginx/html

# 5️⃣ Expose Nginx port
EXPOSE 80

# 6️⃣ Start Nginx
CMD ["nginx", "-g", "daemon off;"]
