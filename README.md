# vscode-compose-template

VS Code Remote Containersのdocker-compose用テンプレート

## 使い方

```
$ touch ui/.env
$ touch server/.env
```

## ui

```
$ create-react-app <project-name> --template typescript
$ rm -rf <project-name>/node_modules
$ mv <project-name> .
$ yarn
```

```
$ yarn add -D eslint prettier eslint-config-prettier 
$ yarn add -D @typescript-eslint/eslint-plugin @typescript-eslint/parser eslint-plugin-react
$ touch .prettierrc
$ touch .eslintrc.json
$ rm .gitignore
```

`.prettierrc`は以下とする
```
{
  "singleQuote": true,
  "semi": false
}

```

`.eslintrc.json`は以下とする
```
{
  "env": {
    "browser": true,
    "es2021": true,
    "node": true
  },
  "extends": [
    "eslint:recommended",
    "plugin:react/recommended",
    "plugin:@typescript-eslint/recommended",
    "prettier"
  ],
  "parser": "@typescript-eslint/parser",
  "parserOptions": {
    "ecmaFeatures": {
      "jsx": true
    },
    "ecmaVersion": 12,
    "sourceType": "module"
  },
  "plugins": ["react", "@typescript-eslint"],
  "rules": {}
}

```


`package.json`の以下を削除
```
  "eslintConfig": {
    "extends": [
      "react-app",
      "react-app/jest"
    ]
  },
```

## server

```
$ express . --no-view
$ npm i
```
