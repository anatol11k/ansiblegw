FROM java:8-jdk-alpine
COPY web_ui.24.jar  /usr/app/
WORKDIR /usr/app/
EXPOSE 15000
CMD ["java", "-jar", "web_ui.24.jar", "--server.port=15000"]
