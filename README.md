# Конфигурация CommitLint

Линтит сообщение коммита а также прогоняет через линтеры код и не дает
закоммитить если будут найдены ошибки

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

Добавьте в `package.json` конфигурацию:

```json
// package.json
"husky": {
  "hooks": {
    "commit-msg": "commitlint -E HUSKY_GIT_PARAMS"
  }
},
```
