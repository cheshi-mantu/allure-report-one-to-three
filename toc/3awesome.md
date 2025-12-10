# His Awesomeness the awesome report

- [x] this awesome report will ultimately replace all others
- [x] All future efforts will be dedicated to this version.
- [x] Used by default for the `generate` command

## The workflow

1. Create config
2. Execute tests
3. Open report // publish report

## Generate results and report

```shell
pnpm allure run --config=./allurerc.mjs -- pnpm test
```
### generate results, generate report

Results

```shell
pnpm test
```

Report

```shell
pnpm allure generate
```



## Open report

```shell
pnpm allure open
```

## Config

```json
    awesomeEpicProjects: {
      import: "@allurereport/plugin-awesome",
      options: {
        reportName: "Epic Projects",
        singleFile: false,
        reportLanguage: "en",
        open: false,
        charts: chartLayout,
        filter: ({ labels }) => labels.find(({ name, value }) => name === "epic" && value === "Projects"),
      },
    },

```


[go back](3selection.md)
