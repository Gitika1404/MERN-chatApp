# 1️⃣ Use Node base image
FROM node:18

# 2️⃣ Set working directory
WORKDIR /app

# 3️⃣ Copy package files and install dependencies
COPY package*.json ./
RUN npm install

# 4️⃣ Copy the rest of the app
COPY . .

# 5️⃣ Expose backend port
EXPOSE 5000

# 6️⃣ Set environment variables (optional)
ENV NODE_ENV=production

# 7️⃣ Start the app
CMD ["node", "src/index.js"]
