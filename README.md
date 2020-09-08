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
on tslib. tslib is needed for compatibility shims used by TypeScript for
CommonJS interoperability and backwards-compatibility with ES5.

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
