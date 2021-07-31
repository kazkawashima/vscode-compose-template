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
$ yarn add -D eslint prettier eslint-config-prettier @typescript-eslint/eslint-plugin @typescript-eslint/parser eslint-plugin-react eslint-plugin-react-hooks
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
    "plugin:@typescript-eslint/recommended",
    "plugin:react/recommended",
    "plugin:react-hooks/recommended",
    "prettier"
  ],
  "rules": { "react/prop-types": "off", "react/react-in-jsx-scope": "off" }
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
