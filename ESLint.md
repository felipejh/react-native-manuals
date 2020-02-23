# Configurando ESLint, Prettier e EditorConfig no React Native

## EditorConfig

Instalar a extensão ```EditorConfig for VS Code```

Na raiz do projeto, gerar o arquivo ```.editorconfig```clicando com o botão direito e ir na opção de gerar.

Deixar o arquivo como abaixo:
```
root = true

[*]
end_of_line = lf
indent_style = space
indent_size = 2
charset = utf-8
trim_trailing_whitespace = true
insert_final_newline = true
```

## ESLint

Instalar o ESlint como dependência de desenvolvimento:
```yarn add eslint -D```

Rodar o ESLint:
```yarn eslint --init```

Selecionar as opções
- ```To check syntax, find problems, and enforce code style```
- ```JavaScript modules (import/export)```
- ```React```
- *... use TypeScript?* ```N```
- Desmarcar *Browser* e *Node*
- ```Use a popular style guide```
- ```Airbnb: https://github.com/airbnb/javascript```
- ```Javascript```
- *Install npm?* ```Y```

Após a instalação, remover o arquivo ```package-lock.json``` e rodar o comando ```yarn```.

Instalar extensões de configuração do *Prettier*
```yarn add eslint-config-prettier eslint-plugin-prettier babel-eslint -D```

Deixar o arquivo ```.eslintrc.js``` como a seguir:
```
module.exports = {
  env: {
    es6: true,
  },
  extends: [
    'plugin:react/recommended',
    'airbnb',
    'prettier',
    'prettier/react'
  ],
  globals: {
    Atomics: 'readonly',
    SharedArrayBuffer: 'readonly',
    __DEV__: 'readonly',
  },
  parser: 'babel-eslint',
  parserOptions: {
    ecmaFeatures: {
      jsx: true,
    },
    ecmaVersion: 2018,
    sourceType: 'module',
  },
  plugins: [
    'react',
    'prettier',
  ],
  rules: {
    'prettier/prettier': 'error',
    'react/jsx-filename-extension':[
      'warn',
      { extensions: ['.jsx', '.js']}
    ],
    'import/prefer-default-export': 'off'
  },
};
```

## Prettier

Na raiz do projeto, criar o arquivo ```.prettierrc```

```
{
  "singleQuote": true,
  "trailingComma": "es5"
  }
```
