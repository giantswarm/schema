# Re-usable JSON schema

This is an experiment started in December 2022. The purpose is to simplify the building schema for [app](https://docs.giantswarm.io/developer-platform/app-platform/) configuration validation and foster alignment between apps.

## How to use

Schema in this repository can be referenced from other schemas via the "raw" GitHub resource URL. Example:

```json
{
    "$schema": "http://json-schema.org/draft-04/schema#",
    "type": "object",
    "properties": {
        "image": {
            "$ref": "https://raw.githubusercontent.com/giantswarm/schema/main/image/v0.0.1.json"
        }
    }
}
```

## Contents

- [Image](image/): To specify a (Docker) container image to use in a container environment, plus additional information like a pull policy (Kubernetes specific).

## Versioning

Each schema is versioned individually. Each scchema file carries its own [semver 2.0.0](https://semver.org/spec/v2.0.0.html) version number in the file name.

Historic versions are kept in the repository default branch, unless we have a good reason to delete a version/file.
