# Usamos una imagen base oficial de Node.js
FROM node:14

# Directorio de trabajo dentro del contenedor
WORKDIR /app

# Copiar los archivos de package.json y package-lock.json al contenedor
COPY package*.json ./

# Instalar las dependencias
RUN npm install

# Copiar el resto del código de la aplicación
COPY . .

# Exponer el puerto en el que la aplicación correrá
EXPOSE 8080

# Comando para iniciar la aplicación
CMD ["npm", "start"]
