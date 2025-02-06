# Usa una imagen base de Node.js para la construcción
FROM node:15-alpine AS build

# Establece el directorio de trabajo
WORKDIR /app

# Copia package.json y package-lock.json
COPY package*.json ./

# Instala dependencias
RUN npm install

# Copia el código fuente
COPY . .

# Construye la aplicación
RUN npm run build

# Usa una imagen más ligera para servir los archivos
FROM node:15-alpine

# Instala `serve`
RUN npm install -g serve

# Copia la aplicación desde la imagen de construcción
COPY --from=build /app/build /app/build

# Expone el puerto 8080
EXPOSE 8080

# Comando para iniciar el servidor
CMD ["serve", "-s", "/app/build", "-l", "8080"]
