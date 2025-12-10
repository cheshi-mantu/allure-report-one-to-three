# And now with information pushed to Jira Software Cloud

| - | - |
|---|---|
| [allure3 repo](https://github.com/allure-framework/allure3/tree/main/packages/plugin-jira)  | ![JSC](allure-jsc.png) |

## the Workflow

1. Install the plug-in
2. Get credentials
3. Update Allure report config

### Config

```text
import { defineConfig } from "allure";

export default defineConfig({
  name: "Allure Report",
  output: "./allure-report",
  historyPath: "./history.jsonl",
  plugins: {
    jira: {
      options: {
        issue: "ARFJ-4",
        webhook: process.env.ALLURE_JIRA_WEBHOOK,
        token: process.env.ALLURE_JIRA_TOKEN,
        uploadReport: true,
        uploadResults: true,
      },
  },
});
```

[back](toc.md)