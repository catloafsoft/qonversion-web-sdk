# Releases And Packages

This repository publishes the package as `@catloafsoft/qonversion-web-sdk` on GitHub Packages and creates a GitHub Release from version tags.

## Creating a release

1. Update the version in `package.json`.
2. Push the release commit to GitHub.
3. Create and push a tag in the format `vX.Y.Z`, for example:

```bash
git tag v1.1.2
git push origin v1.1.2
```

Pushing the tag creates a GitHub Release automatically. The published Release then triggers package publication to GitHub Packages.

## Installing from another repo

Add an `.npmrc` entry so the `@catloafsoft` scope resolves to GitHub Packages:

```ini
@catloafsoft:registry=https://npm.pkg.github.com
//npm.pkg.github.com/:_authToken=${GITHUB_TOKEN}
```

Then install the package:

```bash
pnpm add @catloafsoft/qonversion-web-sdk
```

GitHub Packages npm installs currently require authentication, so use a token with package read access in the consuming repository or environment.
