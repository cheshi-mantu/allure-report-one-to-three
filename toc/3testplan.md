# testplan

### why?

Generates `testplan.json` with list of failed tests for test framework to re-run.

```shell
allure run -- ./gradlew clean test
```

```shell
allure testplan build/allure-results
```

```shell
./clean.sh
```

```shell
export ALLURE_TESTPLAN_PATH=plugin-testplan/testplan.json
```

```shell
echo $ALLURE_TESTPLAN_PATH
```

![magic!!1](magic.png)

```shell
allure run -- ./gradlew clean test
```

- [ ] check the magic

```shell
allure generate build/allure-results
allure open
```
[go back](allure3.md#testplan)