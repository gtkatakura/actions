# actions

Reusable GitHub Actions workflows and composite actions shared by my projects.

## Use

Call a workflow from a project, pinned to a release tag:

```yaml
jobs:
  release:
    uses: gtkatakura/actions/.github/workflows/<workflow>.yml@v1
    with:
      # inputs documented in the workflow file
    secrets: inherit
```

Pin to a tag (`@v1`) or a commit SHA, never to `main`. Breaking changes get a new major tag.

## Workflows

None published yet. The first ones will come out of [WebFrost](https://github.com/gtkatakura/webfrost)'s
release pipeline: building a GitHub Release from per-platform archives and `checksums.txt`, build
provenance attestations, and updating the formula in [gtkatakura/homebrew-tap](https://github.com/gtkatakura/homebrew-tap).

## Conventions

- Inputs and secrets are explicit; nothing here assumes where a project is hosted or deployed.
- Third-party actions are pinned by commit SHA.
- Every workflow sets the smallest `permissions` it needs.

## License

[MIT](LICENSE)
