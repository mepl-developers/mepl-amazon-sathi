# NPM Package Publishing Guide

## Authentication Setup

### Verify NPM Authentication Status

```bash
npm whoami
```

### Login to NPM Registry

If not currently authenticated, execute the following command:

```bash
npm login
```

### Confirm Authentication

Verify successful authentication:

```bash
npm whoami
```

## Versioning Strategy

### Patch Release

For bug fixes and minor updates:

```bash
npm version patch
```

**Example:** `1.0.0` → `1.0.1`

### Minor Release

For new backward-compatible features:

```bash
npm version minor
```

**Example:** `1.0.1` → `1.1.0`

### Major Release

For breaking changes:

```bash
npm version major
```

## Publishing Procedure

### Step 1: Configure NPM Authentication Token

Set up your NPM authentication token:

```bash
npm config set //registry.npmjs.org/:_authToken=YOUR_AUTH_TOKEN
```

Replace `YOUR_AUTH_TOKEN` with your actual NPM authentication token.

### Step 2: Publish Package

```bash
npm publish
```

### Step 3: Create Release Tag

Push the version tag to the repository:

```bash
git push origin main --follow-tags
```
