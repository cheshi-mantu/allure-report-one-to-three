# configs

1. Yes, will be documented
2. Configs allow to set configuration for all modules.
3. Configs allow creation of multi-reports
   1. same report type with different configs (e.g. filters)

## how?

fill the configs in `allurerc.mjs` file

```javascript
import { defineConfig } from "allure";
import { group } from "console";

export default defineConfig({
  name: "Hello everyone",
  output: "001/allure-report",
  plugins: {
    awesome: {
      options: {
        reportName: "Very genuine fake tests, no SMS",
        singleFile: false,
        reportLanguage: "en",
        open: false,
        groupBy: ["epic","feature","story"],
        charts: chartLayout,
      },
    },
    log: {
      options: {
        groupBy: "none"
        },
    }
  }
});
```

[go back](3selection.md)