# tsconfig

Standard TypeScript compiler configuration for Software Ventures Limited.

## Install

```bash
npm install --save-dev @softwareventures/tsconfig
```

or for yarn users:

```bash
yarn add --dev @softwareventures/tsconfig
```

We recommend that all packages that use this configuration also add a dependency
on tslib. tslib is needed to support a handful of languages features that are
available in ES2018+ but not ES2017.

```bash
npm install --save tslib
```

or

```bash
yarn add tslib
```

## Usage

Create a `tsconfig.json` file in the root of your project containing:

```json
{
    "extends": "@softwareventures/tsconfig"
}
```

With the above configuration, TypeScript will generate CommonJS modules.

If you want TypeScript to generate ES2020 modules instead, use the following
configuration:

```json
{
    "extends": "@softwareventures/tsconfig/esm.json"
}
```
