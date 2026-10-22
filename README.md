AbleSpace Manual Testing

Manual QA notes for the AbleSpace staging website. This repository documents exploratory checks, workflow test cases, and issues observed while using the application.

## Application Under Test

- **Name:** AbleSpace
- **Environment:** [Staging](https://staging.ablespace.io/)
- **Testing approach:** Manual exploratory testing through the user interface
- **Test data:** Fictional sample student and organization data where needed

> This project contains no login credentials. Use an authorized staging account to access the application.

## Coverage

The reported checks covered these areas and workflows:

- Signup and login
- Main navigation and Caseload
- Student profile, IEP details, goals, and progress data
- Add Student form
- Notes, Service Time, Accommodations, and Worksheets
- Family Center daily log
- Support resources
- Billing export and session counts
- Organization setup options
- Mobile layout and workflow behavior at a 390 × 844 viewport

This is exploratory coverage, not a claim that every feature or scenario in the application has been tested.

## Reported Results

- Core student workflows were reported as passing in desktop testing for the scenarios exercised.
- In mobile testing, signup/login was reported as passing; the main workflow and Add Student form were reported to lag or crash intermittently.
- A Caseload run confirmed the page loads and student search works. Opening one student profile produced “Something went wrong” notices.
- Existing goal history remained visible after reopening and refreshing the student record. This check used existing saved data; a new progress entry was not saved during that run.
- A billing check showed three rows in the export while Account Settings showed zero sessions.
- Organization setup showed the Skip button overlapping the Info icon details after selecting a setup option.

## Bug Register

The available bug report workbook is:

- [`outputs/ablespace_bug_report_register.xlsx`](outputs/ablespace_bug_report_register.xlsx)

It contains the reported issue details. Add new findings to the register with reproducible steps, expected and actual results, severity, priority, environment, and evidence.

## Suggested Test Record Format

For each manual check, record:

1. Test case ID and title
2. Preconditions and test data
3. Steps performed
4. Expected result
5. Actual result
6. Status: Pass, Fail, Blocked, or Not Run
7. Browser/device and evidence, when available

Only mark a test **Pass** when the observed result meets the expected result. Use **Blocked** or **Not Run** when a prerequisite prevents execution; do not infer an outcome.

## Limitations

- Results reflect the staging application and the data available in the test account at the time of testing.
- Some scenarios depend on existing student goals or saved records.
- Browser version and device details should be recorded alongside each future run; they were not independently verified for every reported result.
- Automated tests are not included in this repository.

