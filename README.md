# Re-usable JSON schema

This is an experiment started in December 2022. The purpose is to simplify the building schema for [app](https://docs.giantswarm.io/developer-platform/app-platform/) configuration validation and foster alignment between apps.

## Contents

- [Image](image/): To specify a (Docker) container image to use in a container environment, plus additional information like a pull policy (Kubernetes specific).

## How to use

Schema in this repository can be referenced from other schemas via the "raw" GitHub resource URL. Example:

```json
{
    "$schema": "http://json-schema.org/draft-04/schema#",
    "type": "object",
    "properties": {
        "image": {
            "$ref": "https://schema.giantswarm.io/image/v0.0.1"
        }
    }
}
```

## schema.giantswarm.io URLs

The content of this repository (main branch only) is served by [schema-server](https://github.com/giantswarm/schema-server) under URLs of the following format:

    https://schema.giantswarm.io/NAME/VERSION

For example:

    https://schema.giantswarm.io/image/v0.0.1

## Adding schema

- Use branches for schema in development.
  - If needed, you can reference a schem in development via `https://raw.githubusercontent.com/giantswarm/schema/BRANCH/PATH`.
- Make sure to set a simple and useful folder name on the top level, using only the characters `[a-z0-9]` and the `-` separator.
- Add a `README.md` file to your folder, explaining how to use the schema etc.
- For a schema release to be published under `schema.giantswarm.io`, name the file in the format `VERSION.json`, where VERSION must match `[0-9]+.[0-9]+.[0-9]+` (this is more restrictive than semver!).
- Maintain `CHANGELOG.md`.

## Versioning

Each schema is versioned individually. Each scchema file carries its own [semver](https://semver.org/spec/v2.0.0.html) version number in the file name. However we only support numeric major, minor and patch version segments.

Historic versions are kept in the repository default branch, unless we have a good reason to delete a version/file.

Changes between versions are tracked in the [changelog](CHANGELOG.md).
