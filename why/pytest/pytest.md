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
