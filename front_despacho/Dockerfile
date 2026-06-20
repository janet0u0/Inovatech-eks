# Etapa 1: Construcción (Build)
FROM node:18 AS build

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

RUN npm run build

# Etapa 2: Servidor Web (Producción)
FROM nginx:stable-alpine

# Copia los archivos construidos a la carpeta de Nginx
COPY --from=build /app/dist /usr/share/nginx/html

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]