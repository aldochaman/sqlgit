FROM mcr.microsoft.com/mssql/server:2019-latest

ENV ACCEPT_EULA=Y
ENV SA_PASSWORD=Aldodock1200

RUN apt-get update && \
    apt-get install -y sudo curl apt-transport-https gnupg && \
    curl https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add - && \
    curl https://packages.microsoft.com/config/ubuntu/20.04/prod.list | sudo tee /etc/apt/sources.list.d/msprod.list && \
    sudo apt-get update && \
    sudo apt-get install -y mssql-tools unixodbc-dev && \
    sudo apt-get clean -y && \
    sudo rm -rf /var/lib/apt/lists/*

ENV PATH="$PATH:/opt/mssql-tools/bin"

EXPOSE 1433

CMD ["/opt/mssql/bin/sqlservr"]
