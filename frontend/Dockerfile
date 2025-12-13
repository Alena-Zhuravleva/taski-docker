# frontend/Dockerfile (самая простая)
FROM node:18-alpine

WORKDIR /app

COPY package*.json ./
RUN npm ci

COPY . .
RUN npm run build

# Команда для копирования в volume
CMD ["sh", "-c", "cp -r /app/build/. /frontend_static/ && tail -f /dev/null"]