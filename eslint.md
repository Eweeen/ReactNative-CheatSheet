# esLint & Prettier

```sh
$ yarn add -D eslint eslint-plugin-prettier eslint-plugin-react-hooks @typescript-eslint/eslint-plugin @typescript-eslint/parser eslint-config-prettier eslint-plugin-react eslint-plugin-react-native prettier
```

Créer les fichiers suivants:

.eslintrc.json

```json
{
  "env": {
    "es2021": true,
    "node": true
  },
  "extends": [
    "plugin:react/recommended",
    "plugin:react-hooks/recommended",
    "prettier"
  ],
  "parserOptions": {
    "ecmaFeatures": {
      "jsx": true
    },
    "ecmaVersion": "latest",
    "sourceType": "module"
  },
  "plugins": ["react", "react-native", "prettier"],
  "rules": {
    "react/react-in-jsx-scope": "off",
    "prettier/prettier": [
      "error",
      {
        "singleQuote": false,
        "endOfLine": "auto",
        "semi": true
      }
    ]
  }
}
```

.eslintignore

```
node_modules/
```

.prettierrc.json

```json
{
  "$schema": "https://json.schemastore.org/prettierrc",
  "semi": true,
  "tabWidth": 2,
  "endOfLine": "auto",
  "printWidth": 100,
  "trailingComma": "none"
}
```
