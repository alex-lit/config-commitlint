# Конфигурация CommitLint

## Установка

```sh
npm i @alexlit/config-commitlint -D
```

## Подключение

Создайте в корне проекта файл `.commitlintrc.js`:

```js
// .commitlintrc.js
module.exports = {
  extends: ["@alexlit/config-commitlint"],
};
```

Для автоматического линтинга и исправления кода при коммите cоздайте в `package.json` конфигурацию:

```json
// package.json
"husky": {
  "hooks": {
    "pre-commit": "lint-staged"
  }
},
"lint-staged": {
  "*.{js,ts,vue}": "eslint --fix",
  "*.{vue,pcss,scss,sass,css}": "stylelint --fix"
},
```
