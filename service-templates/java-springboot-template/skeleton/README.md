# ${{ values.friendly_name }}

${{ values.description }}

## Requirements

- Java ${{ values.java_version }}
- Maven ${{ values.maven_version }}
- Devbox

## Getting Started

```bash
devbox shell
```

## Useful Commands

| Task              | Command |
|-------------------|--------------------------------------------|
| Run App           | mvn spring-boot:run                        |
| Run Tests         | mvn test                                   |
| Lint Code         | mvn checkstyle:check                       |
| Code Coverage     | mvn jacoco:report                          |
| Build JAR         | mvn clean install                          |
| Security Scan     | mvn org.owasp:dependency-check-maven:check |
| Serve MkDocs      | mkdocs serve                               |
| Build MkDocs site | mkdocs build                               |
| Build Tech Docs   | techdocs-cli generate --no-docker          |
