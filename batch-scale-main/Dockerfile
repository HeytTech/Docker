FROM microsoft/aspnetcore:latest
 
# Default Application TCP/Port.
EXPOSE 80
EXPOSE 9001
EXPOSE 9011
 
# Environment variables.
ENV WEB_PORT=80
ENV SERIAL_PORT=/dev/ttyUSB0
 
# Application Volume.
VOLUME [ "/app" ]
 
# Set working dir.
WORKDIR /app
 
# Run Application.
ENTRYPOINT ["dotnet", "BatchScaleController.dll"]
