# Roxabi/.github

Shared GitHub configuration and reusable workflows for the Roxabi organization.

## Publishing container images

All Roxabi projects that ship as containers use a single reusable workflow to build and publish
to GHCR (`ghcr.io/roxabi/<project>`). Two triggers are supported: a push to `staging` produces
a `:staging` floating tag; a release-please tag of the form `<component>/vX.Y.Z` produces
`:X.Y.Z`, `:X`, and `:latest`.

Caller workflow shape (copy and adapt per project):

```yaml
name: publish
on:
  push:
    branches: [staging]
    tags: ['<project>/v*']
permissions:
  contents: read
  packages: write
jobs:
  publish:
    uses: Roxabi/.github/.github/workflows/publish-container.yml@v1
    secrets: inherit
    with:
      image_name: ghcr.io/roxabi/<project>
      release_please_component: <project>
```

Always pin `@v1`. The `v1` branch advances forward only for non-breaking changes.

See the full pattern documentation in Roxabi/lyra:
https://github.com/Roxabi/lyra/blob/main/docs/ops/container-publishing.md
