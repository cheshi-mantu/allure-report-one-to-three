# run

## Completely new stuff

`run` executes the provided command e.g. `gradle clean test`

## Cool stuff

`--rerun N`

like

```shell
allure run --rerun 2 -- ./gradlew test
```

Reruns failed tests using `testplan.json` behind the scenes if configured.