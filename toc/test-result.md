# Once upon a time...

![](../far-far-away.png)

## Java JUnit5 test result

```xml
<?xml version="1.0" encoding="UTF-8"?>
<testsuite name="io.qameta.allure.IssuesRestTest" tests="4" skipped="0" failures="0" errors="0" timestamp="2025-05-16T16:16:32" hostname="gogi-mbp.local" time="0.256">
  <properties/>
  <testcase name="(First Note)" classname="io.qameta.allure.IssuesRestTest" time="0.232"/>
  <testcase name="(Second Note)" classname="io.qameta.allure.IssuesRestTest" time="0.005"/>
  <testcase name="(First Note)" classname="io.qameta.allure.IssuesRestTest" time="0.002"/>
  <testcase name="(Second Note)" classname="io.qameta.allure.IssuesRestTest" time="0.003"/>
  <system-out><![CDATA[]]></system-out>
  <system-err><![CDATA[]]></system-err>
</testsuite>
```


## Pytest Test Results

```shell
```shell
============================= test session starts ==============================
platform darwin -- Python 3.13.3, pytest-8.3.3, pluggy-1.5.0
rootdir: /Users/egorivanov/code/allure-pytest-github
configfile: pytest.ini
plugins: allure-pytest-2.13.5
collected 9 items

test/issue_rest_test.py ....                                             [ 44%]
test/issues_web_test.py ..F                                              [ 77%]
test/pullrequests_web_test.py ..                                         [100%]

=================================== FAILURES ===================================
_________________________ test_should_add_note_to_ads __________________________

web_driver = None

    @tm4j("AE-T4")
    @microservice("Repository")
    @allure.story("Create new issue")
    @jira_issues("7")
    @pytest.mark.web
    @pytest.mark.regress
    @allure.title("Adding note to advertisement")
    def test_should_add_note_to_ads(web_driver):
        steps.open_issues_page(OWNER, REPO)
>       steps.create_issue_with_title(ISSUE_TITLE)

test/issues_web_test.py:61: 
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 
test/steps/web_steps.py:40: in create_issue_with_title
    maybe_throw_assertion_exception(title)
_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 

text = 'Some issue title here'

    def maybe_throw_assertion_exception(text):
        if is_time_to_trow_exception():
>           pytest.fail(text_equal.format(expected=text, actual="another text"))
E           Failed: Element should text 'Some issue title here' {By.xpath: //a[@href='/eroshenkoam/allure-example']}
E           Element: '<a class="v-align-middle">another text</a>'
E           Screenshot: file:/Users/eroshenkoam/Developer/eroshenkoam/webdriver-coverage-example/build/reports/tests/1603973703632.0.png
E           Page source: file:/Users/eroshenkoam/Developer/eroshenkoam/webdriver-coverage-example/build/reports/tests/1603973703632.0.html
E           Timeout: 4 s.

test/steps/web_steps.py:89: Failed
=========================== short test summary info ============================
FAILED test/issues_web_test.py::test_should_add_note_to_ads - Failed: Element...
========================= 1 failed, 8 passed in 7.10s ==========================
```

- Please send the team of interpreters!


[back](./toc.md#the-agenda-for-todays-webinar)