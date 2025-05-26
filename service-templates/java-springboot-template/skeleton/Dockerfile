# Build Stage
FROM maven:{{values.maven_version}}-eclipse-temurin-{{values.java_version}} AS build
WORKDIR /workspace
COPY . .
RUN mvn clean package -DskipTests

# Runtime Stage (minimal image, optimized layers)
FROM eclipse-temurin:{{values.java_version}}-jre-alpine

ENV APP_HOME=/app
WORKDIR ${APP_HOME}

# Copy only layers and launcher
COPY --from=build /workspace/target/{{values.project_slug}}-*.jar app.jar
RUN java -Djarmode=layertools -jar app.jar extract

# Default command (override via CMD or ENTRYPOINT)
ENTRYPOINT ["java", "-cp", "BOOT-INF/classes:BOOT-INF/lib/*", "org.springframework.boot.loader.JarLauncher"]