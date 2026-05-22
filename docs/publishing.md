# Publishing Guide

## Prerequisites

- npm account with 2FA enabled
- Membership in `@lowwattlabs` org on npm
- Verified email

## Release Process

1. Update version in all package.json files
2. Build all packages: `npm run build`
3. Test all packages: `npm test`
4. Dry run: `npm publish --dry-run` from each node directory
5. For real publish: `./scripts/publish-all.sh`

## Versioning

- Follow semver: MAJOR.MINOR.PATCH
- Breaking API changes = MAJOR bump
- New operations/features = MINOR bump
- Bug fixes = PATCH bump

## First-Time Setup

```bash
# Login to npm
npm login

# Create org (if not done)
npm org create lowwattlabs

# Verify packages are under org scope
npm config set scope lowwattlabs
```

## Checklist Before Publishing

- [ ] All tests pass
- [ ] README updated with current operations
- [ ] package.json version bumped
- [ ] CHANGELOG.md updated
- [ ] No console.log or debug statements
- [ ] dist/ rebuilt and committed