# Platform Backstage Templates

This repository contains a curated set of [Backstage](https://backstage.io/) Software Templates used to bootstrap standardized service repositories, infrastructure configurations, and organizational metadata across our platform.

These templates power the **Create** functionality in our internal Backstage developer portal.

## Repository Structure

```bash
└── service-templates/      # Templates for creating new application or service repos
    └── java-springboot-template/
        ├── skeleton/
        │   ├── ...
        └── template.yaml
├── infra-templates/        # Infrastructure scaffolding (e.g., EKS clusters, S3 buckets)
├── metadata-templates/     # Templates for domains, systems, groups, etc.
├── catalog-info.yaml       # Template registration for Backstage catalog
├── README.md
```

## Available Templates

| Template Name | Description   | Location  |
|---------------|---------------|-----------|
| `java-springboot-template`    | Scaffolding a Spring Boot microservice with shared CI | `service-templates/java/springboot-template/` |
| _More coming soon..._         | Other tech stacks |   |

## Using Templates in Backstage

To use these templates, make sure your Backstage instance is configured to reference this repository.
