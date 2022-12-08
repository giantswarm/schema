### What does this PR do?

(Please set a descriptive PR title. Use this space for additional explanations.)

### Any background context you can provide?

(Please link public issues or summarize if not public.)

### Are you meeting our versioning requirements?

- In general, all schema modifications are done by creating a new version and new file.
- Changes that can lead to breaking validation (where the payload was valid with the previous version) require a **major** version bump.
- Non-breaking changes like additions should yield a new **minor** version.
- Only smallest changes should be published as **patch** version bump, e. g. a typo fix in a `title` or `description` field.

### Have you also followed these requirements?

- [ ] I have requested reviews from several teams.
- [ ] I updated CHANGELOG.md.
- [ ] I checked/maintained the README.md within the schema folder.
