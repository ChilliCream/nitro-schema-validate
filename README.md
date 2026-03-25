# Nitro Schema Validate

A GitHub Action that validates GraphQL schemas against the Nitro registry.

## Usage

```yaml
- uses: ChilliCream/nitro-schema-validate@v16
  with:
    stage: <stage>
    api-id: <api-id>
    schema-file: ./schema.graphql
    api-key: <api-key>
```

## Inputs

| Name          | Required | Description                                              |
| ------------- | -------- | -------------------------------------------------------- |
| `stage`       | Yes      | The name of the stage                                    |
| `api-id`      | Yes      | The ID of the API                                        |
| `schema-file` | Yes      | The path to the graphql file with the schema definition  |
| `api-key`     | Yes      | API key for authentication                               |
| `cloud-url`   | No       | The URL of the Nitro registry                            |

The action automatically attaches source metadata from the GitHub Actions runtime.

If you self-host Nitro or use a dedicated hosted instance, you can specify the `cloud-url` input to point to your instance.
