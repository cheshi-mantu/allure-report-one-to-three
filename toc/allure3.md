# Allure 3

## Issues to be resolved

1. You are JS/TS and suddenly you need Java to see the report.
   1. what?!
   ![now and then](./now-and-then.png)
2. Modern Technology stack
   1. `npm install allure`
   2. `npx allure`
3. Avoid the generation of a full report each time
   1. different commands for different tasks

- [ ] use `--help` to see what is available.

```shell
Commands:
  classic <resultsDir>       Generates Allure 2 report based on provided Allure Results // will be discontinued
  allure2 <resultsDir>       Generates Allure 2 report based on provided Allure Results  // will be discontinued
  awesome <resultsDir>       Generates Allure Awesome report based on provided Allure Results // this is the future
  csv <resultsDir>           Generates CSV report based on provided Allure Results
  dashboard <resultsDir>     Generates Allure Dashboard report based on provided Allure Results // WIP
  generate <resultsDir>      Generates the report to specified directory based on provided config (if any)
  history <resultsDir>       Generates the history to specified folder
  known-issue <resultsDir>   Generates a known issue list
  log <resultsDir>           Prints Allure Results to the console
  open [reportDir]           Serves specified directory
  quality-gate <resultsDir>  Returns status code 1 if there any test failure above specified success rate
  run                        Run specified command
  slack <resultsDir>         Posts test results into Slack Channel
  testplan <resultsDir>      Generates testplan.json based on provided Allure Results
  watch <resultsDir>         Watches Allure Results changes in Real-time
```

4. We need plug-ins!!!
   1. Now it's easier to build plug-ins.

## Commands

### Completely new stuff

#### run

[run - check this out](3run.md)

#### testplan

[testplan - check this out](3testplan.md)

#### log

[log - check this out](3log.md)

#### csv

[csv - check this out](3csv.md)

#### history

[history - check this out](3history.md)

#### watch

[watch - check this out](3watch.md)

### New HTML report - His Awesomeness the Awesome

#### awesome

[AWESOME - check this out](3awesome.md)

### Configuration files

[configs - check this out](3configs.md)

## What's next?

[What's next?](3whatsnext.md)


## Plugins

No stop here today. Still, here is an example of a plugin that will send a message to telegram.

![](qr-tlg-send-plugin.png)

[back to TOC](toc.md)
