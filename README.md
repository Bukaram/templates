

A 
  -w, --workspace-folder  Target workspace folder to apply Template                   [string] [required] [default: "."]
  -t, --template-id       Reference to a Template in a supported OCI registry                        [string] [required]
  -a, --template-args     Arguments to replace within the provided Template, provided as JSON   [string] [default: "{}"]
  -f, --features          Features to add to the provided Template, provided as JSON.           [string] [default: "[]"]
      --log-level         Log level.                               [choices: "info", "debug", "trace"] [default: "info"]
      --tmp-dir           Directory to use for temporary files. If not provided, the system default will be inferred.
                                                                                                                [string]
```

#### Example

```
devcontainer templates apply --workspace-folder . \
    --template-id ghcr.io/devcontainers/templates/cpp:latest \
    --template-args '{ "imageVariant": "debian-12" }' \
    --features '[{ "id": "ghcr.io/devcontainers/features/azure-cli:1", "options": { "version" : "1" } }]'
```

## Contributions

### Creating your own collection of templates

The [Dev Container Template specification](https://containers.dev/implementors/templates-distribution/#distribution) outlines a pattern for community members and organizations to self-author Templates in repositories they control.

A starter repository [devcontainers/template-starter](https://github.com/devcontainers/template-starter) and [GitHub Action](https://github.com/devcontainers/action) are available to help bootstrap self-authored Templates.

We are eager to hear your feedback on self-authoring!  Please provide comments and feedback on [spec issue #71](https://github.com/devcontainers/spec/issues/71).

### Contributing to this repository

This repository will accept improvement and bug fix contributions related to the
[current set of maintained templates](./src).

## Feedback

Issues related to these templates can be reported in [an issue](https://github.com/devcontainers/templates/issues) in this repository.

# License
Copyright (c) Microsoft Corporation. All rights reserved. <br />
Licensed under the MIT License. See [LICENSE](LICENSE).