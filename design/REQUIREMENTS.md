# Main Features
- Projects
- Test Plans
- Test Suites
- Test Cases
    - Snippets
    - Description Templates
    - Creation Templates
- Test Runs

# Projects
The point of a project is to contain anything related to one project, whether it be mobile, web, or hardware. It really isn't that interesting of a concept.

At bare minimum a user should be able to:
- Create new projects with a:
    - Title
    - Description
- Delete projects
- View who created a project
- View when the project was created
- View project statistics, such a summary about all the items the project contains

All other test related data that goes inside a test plan should be available by specifying the test plan.

# Test Plans
A test plan should hold a collection of test suites or test cases. The goal of it is to contain data that you would like to later create a test run out of. Some examples could be a test plan for a product release or something like a smoke test to ensure that major components are still working.

At bare minimum a user should be able to:
- Create new test plans with a:
    - Title
    - Description
- View who created a test plan
- View when the test plan was created
- Add test cases to it
- Add test suites to it
- Remove test cases from it
- Remove test suites from it
- Display a list of test suites/cases in it
- Allow for ordering of test suites/cases in a static way, this is in the case that I want to have some more critical/basic tests listed first
- View test plan statistics, such a summary about all the items the project contains
  
Test plans should also:
- Record a history of actions that a user has performed such as:
    - Added tests to it
    - Removed tests from it

# Test Suites
A basic grouping of tests.
At bare minimum a user should be able to:
- Create new test suite with a:
    - Title
    - Description
- View who created a test suite
- Add test cases to it
- Remove test cases from it
- Display a list of test cases in it
- Allow for ordering of test cases in a static way, this is in the case that I want to have some more critical/basic tests listed first

# Test Cases
A test case should hold various information about how to reproduce a test and the history associated with it. It should have info such as:
- Author
- Title
- Description (the default text for this should be via description templates)
- Labels
- Priority
- Version
- What test suites it's featured in
- What test plans it's featured in
- Last outcome from test runs
- Date created

## Snippets

Test case snippets should be some text that you want to insert into your test case description. Think of them as blocks of simple text that you can reference in your test cases in order to cut down on the amount of text you need to write. The most typical example for them would be the use of setup and teardown for a test case.

A test case snippet should have info such as:
- Author
- Title
- Description
- Date created

**It's currently undecided if test snippets should allow for nesting**

Modifying a test snippet itself should also be reflected in where ever the test snippet is featured, that is to say, adding a snippet to a test case should not directly modify the test case itself with all the info from the snippet.

## Description Templates
Description Templates should allow the description of a test case to have some preformatted text inside the description. This is so that you can have stuff like Setup/Teardown headers in the description without adding the manually each time.

Need to decide at what level description templates would reside in, test plan, test suite, both? This likely won't matter for the API design too much.

## Creation Templates
Creation templates should be the template that test cases are based off of. It may be that the default fields are not sufficient for all uses cases, for example while designing it I almost totally forgot to include `Priorty` as one of the needed fields. As an end user I should be able to control what are the fields that get shown for a test case.

I'm sure this feature is going to be nightmare.

# Test Runs
Test Runs should be created from test plans. Each test case/suite should get "cloned" into a test plan whereby the test cases can be marked as Pass, Fail, Skip, Not Applicable, etc. Perhaps the snippet system could be used here for a whole case so that it's not the whole data that gets cloned in the DB.





