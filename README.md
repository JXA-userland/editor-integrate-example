# Editor integrate example repository

## Usage

You can try to open this repository with * [Visual Studio Code](https://code.visualstudio.com/ "Visual Studio Code - Code Editing. Redefined")

    git clone https://github.com/JXA-userland/editor-integrate-example
    cd editor-integrate-example
    vscode .

**limitation**

Some types is `any`.
It means that does not work auto complate for all object.

## Reproduce steps

1. Create `package.json`
  - `$ npm init --yes` 
2. Install `@jxa/global-type`
  - `$ npm install -D @jxa/global-type`
3. Adding [`tsconfig.json`](http://www.typescriptlang.org/docs/handbook/tsconfig-json.html) file with the following configuration should get intelligent code completion working.

**tsconfig.json:**
```json5
{
  "compilerOptions": {
    "allowJs": true,
    "types": [
      "@jxa/global-type"
    ]
  },
  "include": [
    "**/*.js" // <= this scope is integrated with @jxa/global-type
  ]
}
```

For more details, see [@jxa/global-type](https://github.com/JXA-userland/JXA/tree/master/packages/@jxa/global-type).