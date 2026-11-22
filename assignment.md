
## Part 1: Create a Test Plan

| Requirement | Description |
| --- | --- |
| Test Objectives | Verify that the Counter application correctly increments, decrements, and resets the displayed count based on user input. |
| In Scope | Increment, Decrement, and Reset button functionality; initial counter value |
| Out of Scope | Visual design, accessibility, performance/load testing, and backend functionality. |
| Testing Approach | Manual black-box functional testing using positive tests and sequences of button interactions. Compare the displayed count against expected results. |
| Test Environment | Local React/TypeScript application running through Vite in a desktop web browser. |
| Testing Tools | Web browser and manual test case documentation in assignment.md. |
| Product Risk | Incorrect counter calculations or state updates could cause the displayed value to become inaccurate, especially after multiple button interactions. |
| Entry Criteria | The application runs successfully, the counter is displayed, and all three buttons are accessible. |
| Exit Criteria | All planned test cases have been executed, actual results are documented, and any failed tests are repeated and reported as defects. |


## Part 2: Design Test Cases

| Test Case ID | Starting State | Actions | Expected Result |
| --- | --- | --- | --- |
| TC-001 | Application is first opened | Observe the page | Counter displays 0 |
| TC-002 | Counter displays 0 | Click Increment once | Counter displays 1 |
| TC-003 | Counter displays 0 | Click Decrement once | Counter displays -1 |
| TC-004 | Counter displays 5 | Click Reset once | Counter displays 0 |
| TC-005 | Counter displays 0 | Click Increment three times, Decrement once, then Reset | Counter displays 1, 2, 3, 2, and finally 0 |

## Part 3: Execute the Tests

| Test Case ID | Actual result | Pass or fail | 
| --- | --- | --- |
| TC-001 | Counter displays 0 | Pass |
| TC-002 | Counter displays 1 | Pass |
| TC-003 | Counter displays 1 | Fail |
| TC-004 | Counter displays 0 | Pass |
| TC-005 | Counter displays 1, 2, 3, 4, and finally 0 | Fail |
 
*fails are reapeatable*


## Part 4: Report a Defect

| Field | Information |
| --- | --- |
| Defect ID | BUG-001 |
| Title | Decrement button increases counter instead of decreasing |
| Related Test Case | TC-003, TC-005 |
| Test Environment | Local development environment, application running in web browser |
| Steps to Reproduce | 1. Open the application.<br>2. Verify the counter displays 0.<br>3. Click the `Decrement` button.<br>4. Observe the displayed count. |
| Expected Result | Counter decreases by 1, displaying -1. |
| Actual Result | Counter increases by 1, displaying 1. |
| Severity | Medium |
| Priority | High |
| Status | New |

