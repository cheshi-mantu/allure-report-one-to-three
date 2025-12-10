# GH action



| +  | +  |
|---|---|
|[Create PR, and see how it went.](https://github.com/marketplace/actions/allure-report-official)|![](allure-action.png)| 

## pipeline config

```yaml
permissions:
  id-token: write
  pull-requests: write
  checks: write

<SOMETHING>

      - name: Allure Report Official
        uses: allure-framework/allure-action@v0
        with:
          report-directory: "./allure-report"
          github-token: ${{ secrets.GITHUB_TOKEN }}
```

## And action in action

[Check this out!](https://github.com/cheshi-mantu/pw-allure-three-features/pull/3)

[go back](3selection.md)