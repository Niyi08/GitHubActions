# Usa una imagen base de Node.js
FROM node:14

# Definir el directorio de trabajo dentro del contenedor
WORKDIR /app

# Copiar los archivos package.json y package-lock.json
COPY codebase/rdicidr-0.1.0/package*.json /app/

# Instalar las dependencias
RUN npm install

# Copiar el resto de la aplicación
COPY codebase/rdicidr-0.1.0/ /app/

# Exponer el puerto que usará la aplicación
EXPOSE 8080

# Definir el comando para iniciar la aplicación
CMD ["npm", "start"]