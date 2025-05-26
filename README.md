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

Example catalog entry:

```yaml
apiVersion: backstage.io/v1alpha1
kind: Location
metadata:
  name: platform-templates
spec:
  type: url
  target: https://github.com/my-org/platform-backstage-templates/blob/main/catalog-info.yaml
```

Then run:

```bash
yarn catalog:import
```

Or use the __Import__ feature in the Backstage UI.

## Adding a New Template

1. Create a new folder under the appropriate section (e.g., service-templates/my-template/).
1. Add a template.yaml and a skeleton/ directory.
1. Update catalog-info.yaml to include your new template.
1. Test locally using a Backstage instance.
1. Open a PR for review and merge.

## Contributing

We welcome contributions from platform and application teams!

- Folow naming and directory conventions
- Use Nunjucks templating syntax ({{ values.xyz }}) in skeleton files
- Keep templates modular and organization-compliant
