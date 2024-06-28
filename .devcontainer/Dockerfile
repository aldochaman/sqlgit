FROM mcr.microsoft.com/mssql/server:2019-latest

ENV ACCEPT_EULA=Y
ENV SA_PASSWORD=YourStrong!Passw0rd

# Instalar mssql-tools
RUN apt-get update && \
    apt-get install -y mssql-tools && \
    apt-get clean -y

# Agregar mssql-tools al PATH
ENV PATH="$PATH:/opt/mssql-tools/bin"

EXPOSE 1433

CMD ["/opt/mssql/bin/sqlservr"]
