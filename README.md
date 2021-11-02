## Hastscript Test

## Update
This was created to solve [an isuue first noticed](https://github.com/syntax-tree/hastscript/issues/16) in a package that uses Typescript. The issue was that Typescript failed to import `*.d.ts` files without explicitly including the extension. I have only tested this error in TypeScript `4.5.0-beta`.

This issue has been [resovlved](https://github.com/tvquizphd/hastscript-test/pull/2) by adding the following key to `compilerOptions` in `tsconfig.json`:

```
"moduleResolution": "node"
```

This parameter changes how Typescript resolves module names. See [here](https://www.typescriptlang.org/docs/handbook/module-resolution.html) for more.


### Install and Build

```
yarn i && build
```
