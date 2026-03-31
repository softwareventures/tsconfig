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
on tslib. tslib is needed to support a handful of language features that are
available in ES2021+ but not ES2020.

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

The above is the default configuration, which will include the ES2020 API. This
configuration is suitable for projects that target node alone, or that target
both node and the browser.

Several alternative configurations are also provided with settings suitable for
other target environments or module formats. To use one of the alternative
configurations, set the `extends` field to one of the values in the table below.

| `extends`                              |                                                                                                                                               |
| -------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| `@softwareventures/tsconfig`           | The default configuration. Includes ES2020 API. Suitable for projects that either target node alone, or target both node and the browser.     |
| `@softwareventures/tsconfig/dom`       | Includes DOM API in addition to ES2020. Suitable for use in code targeting browsers or for projects that include a DOM library such as jsdom. |
| `@softwareventures/tsconfig/webworker` | Includes WebWorker API in addition to ES2020. Suitable for use in code that will run as a Web Worker.                                         |

All configurations target node16 modules and use node16 module resolution. This
means that TypeScript will either generate CommonJS or ES modules, depending on
the `module` field in your `package.json`.
