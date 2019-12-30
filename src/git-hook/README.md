# Git Hook

See detail [here](https://github.com/typicode/husky)

```shell
npm install husky --save-dev
```

```json
// package.json
{
  "husky": {
    "hooks": {
      "pre-commit": "npm test",
      "pre-push": "npm test",
      "...": "..."
    }
  }
}
```

```shell
git commit -m 'Keep calm and commit'
```