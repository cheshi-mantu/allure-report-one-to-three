# watch

![watch](watch.png)

### why?

Local development without repeating actions.

instead of generating report after each local build

```shell
allure watch --config=./allurerc.mjs --name "Local build watch" ./allure-results
```

then

```shell
pnpm test
```

... and repeat ...

```shell
pnpm test
```

## Usage

1. Local development.
2. Stop local execution if everything went south.

[go back](3selection.md)