# configs

1. Yes, will be documented
2. Configs allow to set configuration for all modules.
3. Configs allow to create multi-reports

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
        reportName: "Awesome report",
        singleFile: true,
		groupBy: ["msrv", "feature","story"]
      },
    },
    classic: {
      options: {
        reportName: "Classic Allure2 like report",
        singleFile: true,
        reportLanguage: "es",
		groupBy: ["msrv", "feature"]
      },
    }, 
    log: {
      options: {
        groupBy: "none"
        },
    },
    csv: {
      options: {
        fileName: "allure-report.csv",
      }
    }
  }
});
```













[go back](allure3.md#watch)