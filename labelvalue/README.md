# Label value

Schema for a label value as defined in Kubernetes metadata.

See https://kubernetes.io/docs/concepts/overview/working-with-objects/labels/#syntax-and-character-set for an upstream definition.

## Possible improvements

- Better `pattern` for string validation, to catch leading and trailing separators.
  
  We tried `"pattern": "^(?![-_\\.])([a-zA-Z0-9-_\\.]{0,63})(?<![-_\\.])$"`, but not all parsers support negative lookaheads.
