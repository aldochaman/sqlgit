# Utilizar la imagen base de SQL Server 2019 de Microsoft
FROM mcr.microsoft.com/mssql/server:2019-latest

# Variables de entorno para la configuración de SQL Server
ENV ACCEPT_EULA=Y
ENV SA_PASSWORD=1220

# Instalar mssql-tools
RUN apt-get update && \
    apt-get install -y mssql-tools && \
    apt-get clean -y

# Agregar mssql-tools al PATH
ENV PATH="$PATH:/opt/mssql-tools/bin"

# Exponer el puerto 1433 para conexiones TCP/IP
EXPOSE 1433

# Comando para iniciar SQL Server al ejecutar el contenedor
CMD ["/opt/mssql/bin/sqlservr"]
