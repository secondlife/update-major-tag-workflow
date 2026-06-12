# update-major-release-workflow

Bump the major semver tag (such as `v1`) on a repository when a new release (such as `v1.0.2`) is published. Example:

``` yaml
# .github/workflows/release.yaml
name: Release

on:
  release:
    types: [published]

permissions:
  # Grant permission to push tags.
  contents: write

jobs:
  update-major-tag:
    uses: secondlife/update-major-tag-workflow/.github/workflows/update-major-tag.yaml@v1
```
