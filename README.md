# update-major-release-workflow

A small shared workflow to bump major semver tag (ex `v1`) on a repository when
a new release (ex. `v1.0.2`) is published. Example use:

```yaml
# .github/workflows/update-major-tag.yaml

name: Update Major Tag

on:
  release:
    types: [published]

jobs:
  tag:
    uses: secondlife/update-major-tag-workflow/.github/workflows/update-major-tag.yaml@v1
```
