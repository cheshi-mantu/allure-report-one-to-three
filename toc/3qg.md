# run + quality gate

`run` executes the provided command e.g. `pnpm test`

## Cool stuff – quality gate

### Config

```text
qualityGate: {
	rules: [
		{
		maxFailures: 3,
		fastFail: true,
		},
	],
},
```

something more complex

```text
qualityGate: {
    rules: [
      {
        maxFailures: 5,
        minCriticals: 5,
        fastFail: true,
      },
      {
        maxFailures: 5,
      },
    ],
    use: [
      maxFailuresRule,
      minCriticalsRule,
    ],
```

and you need to create custom rule for detecting the QG failure

```typescript
import { type QualityGateRule } from "@allurereport/plugin-api";

export const maxFailuresRule: QualityGateRule<number> = {
  rule: "maxFailures",
  message: ({ actual, expected }) =>
    `The number of failed tests ${String(actual)} exceeds the allowed threshold value ${String(expected)}`,
  validate: async ({ trs, knownIssues, expected, state = 0 }) => {
    const knownIssuesHistoryIds = knownIssues.map(({ historyId }) => historyId);
    const unknown = trs.filter((tr) => !tr.historyId || !knownIssuesHistoryIds.includes(tr.historyId));
    const failedTrs = unknown.filter(filterUnsuccessful);
    const actual = failedTrs.length + state;

    return {
      success: actual <= expected,
      actual,
      expected,
    };
  },
};
```

1. Run tests
2. Collect failed tests and save to `testplan.json`
3. Run tests again using `testplan.json`

### Execution

```shell
pnpm allure run --config=./allurerc.mjs -- pnpm test
```

[Example here](https://github.com/cheshi-mantu/pw-allure-three-features/actions)

[go back](3selection.md)