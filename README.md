# react-native-typescript-starter
a react-native project created by typescript and antd-mobile

# Prerequisites
You should first ensure that you can run a plain React Native app without TypeScript. Follow the instructions on the React Native website to get started. When you've managed to deploy to a device or emulator, you'll be ready to start a TypeScript React Native app.

# Getting Started
Recommended use yarn to manage NPM packages.

* Install and Initialization
```bash
$ npm install yarn -g
$ yarn 
$ tsc
# Note : tsc is the command to compile .tsx or .ts files. If it doesn't work, please try: $ npm install -g typescript first.
$ react-native run-android

```
# Introducing TypeScript
Let's create a `tsconfig.json`:
```json
{
    "compilerOptions": {
        "target": "es2015",
        "module": "commonjs",
        "jsx": "react-native",
        "declaration": "true",
        "outDir": "./dist/",
        "strict": true,
        "allowSyntheticDefaultImports": true
    },
    "include": ["./src/"]
}
```

# import antd-mobile
You should have the following steps.
```bash
$ yarn add react-dom --save
$ yarn add antd-mobile --save
$ yarn add babel-plugin-import --save-dev
```
Then modify the .babelrc config like this:

```json
{
  "presets": ["react-native"],
  "plugins": [["import", { "libraryName": "antd-mobile" }]],
  "env": {}
}
```
# use:

  ```js
  ...
  import { Button } from 'antd-mobile';

  ...
  render() {
    return (
      ...
      <Button>antd-mobile button</Button>
      ...
    );
  }
  ```







