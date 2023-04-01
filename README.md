# example-npm-github-package

## Usage

### 1. Authenticating to GitHub Packages

Create `.npmrc` in your PROJECT_ROOT

```
//npm.pkg.github.com/:_authToken=<YOUR_GITHUB_TOKEN>
```

1. Please to https://github.com/settings/tokens
2. Generate new token
3. Selected read:packages [required]
4. Generate Token
5. Copy the generated token and paste it into your YOUR_GITHUB_TOKEN in `.npmrc`

ref: https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-npm-registry

### 2. Create registry config

### with npm

Add a registry to the end of `.npmrc` in PROJECT_ROOT

```
//npm.pkg.github.com/:_authToken=<YOUR_GITHUB_TOKEN>
"@tsubasa:registry" "https://npm.pkg.github.com"
```

### with yarn

Create `.yarnrc` in your PROJECT_ROOT

```
"@tsubasa:registry" "https://npm.pkg.github.com"
```

### 3. Install package

```sh
$ npm install @tsubasa/example-npm-github-package
$ yarn add @tsubasa/example-npm-github-package
```

### 4. Import JS/TS

```typescript
import Hello from '@tsubasa/example-npm-github-package'

Hello('foo');
// Hello, foo!
```
