# run

`run` executes the provided command e.g. `pnpm test`

## Cool stuff – rerun

`--rerun N`

like

```shell
allure run --rerun 2 -- pnpm test
```

1. Run tests
2. Collect failed tests and save to `testplan.json`
3. Run tests again using `testplan.json`


[Quality Gates](3qg.md)

[go back](allure3.md#run)