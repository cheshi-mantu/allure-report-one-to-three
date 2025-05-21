# watch

![watch](watch.png)

### why?

Local development on a loop

```shell
./gradlew clean test
```

instead of generating report after each local build

```shell
allure watch --name "Local build watch" build/allure-results
```

And repeat

```shell
./gradlew clean test
```


[go back](allure3.md#watch)