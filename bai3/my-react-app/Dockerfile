# ===== Stage 1: Build React =====
FROM node:18-alpine AS build

WORKDIR /app

COPY package.json package-lock.json ./

RUN npm install

COPY . .

RUN npm run build


# ===== Stage 2: Serve bằng Nginx =====
FROM nginx:alpine

# Copy build từ stage 1
COPY --from=build /app/build /usr/share/nginx/html

# Mở port 80
EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]