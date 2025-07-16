# reproduce-peerdep-issue

Steps to reproduce:

1. Run `npm i`
2. Run `npm i -E @typescript-eslint/eslint-plugin@8.37.0 @typescript-eslint/parser@8.37.0 typescript-eslint@8.37.0`

NOTE: This does **not** happen if instead of running with `-E` you simply run:

```
npm i @typescript-eslint/eslint-plugin @typescript-eslint/parser typescript-eslint
```

**but**, once you encounter the error caused by #2 above, running even the command without exact versions no longer works even though: `package.json` and `package-lock.json` are identical.
