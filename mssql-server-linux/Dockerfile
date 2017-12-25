FROM microsoft/mssql-server-linux:latest

# Default SQL Server TCP/Port.
EXPOSE 1433

# Environment variables
ENV ACCEPT_EULA=Y
ENV MSSQL_PID=Express
ENV MSSQL_COLLATION=Turkish_CI_AS
ENV MSSQL_SA_PASSWORD=

# Data Volume
VOLUME [ "/var/opt/mssql" ]

# Run SQL Server process.
CMD /opt/mssql/bin/sqlservr