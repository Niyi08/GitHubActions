# Usamos una imagen base oficial de Node.js
FROM node:14

# Directorio de trabajo dentro del contenedor
WORKDIR /app

# Copiar el archivo package.json desde la ubicación correcta
COPY ./codebase/rdicidr-0.1.0/package.json . 

# Instalar las dependencias
RUN npm install

# Copiar el resto del código de la aplicación
COPY ./codebase/rdicidr-0.1.0 . 

# Exponer el puerto en el que la aplicación correrá
EXPOSE 8080

# Comando para iniciar la aplicación
CMD ["npm", "start"]
