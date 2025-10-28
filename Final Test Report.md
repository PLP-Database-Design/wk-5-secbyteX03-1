# 🧪 Final Group Test Report Template — Word Puzzle Game Plus

**Level:** Intermediate QA | **Week 5:** Test Management

**Course:** Software Testing & Quality Assurance  
**Module:** Test Management (Week 5)  
**Project Type:** Group Assessment  
**Submission Date:** 2025-10-28

## Team Information

| Role | Name | Responsibilities |
|------|------|------------------|
| Test Manager | Jackline Cherotich| Planning, scheduling, coordination, metric tracking |
| Risk Analyst | Magret Faith| Risk identification, prioritization, test design linkage |
| Test Executor | Amobigold Sikirat | Execution, evidence capture, defect logging |

## Group Rules

- Each student must belong to only one group.
- Duplicate membership or multiple submissions will result in invalidation.
- Every group member must contribute towards this project

## Project Overview

**System Under Test:** Word Puzzle Game Plus  
**Technology Stack:** HTML, CSS, JavaScript  
**Environment:** Chrome Browser (Desktop)

### Features Under Test

| Feature | Description | Risk Category |
|---------|-------------|---------------|
| Reset Game | Clears score and progress instantly | Medium - state management|
| Leaderboard | Stores top 3 scores in localStorage | High -data persistence|
| Bonus Round | Every 3 puzzles → doubles score |High - business logic |
| Hint | Provides clues at point cost |Medium - scoring logic |
| Word Scrambling | Randomizes word order |Medium - game logic |
| Input Validation | Prevents invalid input |Medium - input validation |
| UI Responsiveness | Handles different screen sizes |Medium - responsiveness |
| Code Maintainability | Maintainable code structure |Medium - maintainability |

## Test Plan

### Objectives

- Validate Leaderboard functionality that it displays top scores and data persists
- Verify core game functionality — word scrambling, bonus calculations, and reset behavior
- Confirm negative test cases (invalid input, no word entered) are handled gracefully
- Evaluate UI responsiveness across various screen sizes and environments
- Apply risk-based testing to prioritize high impact areas
- Document identified defects and provide evidence

### Scope

**In Scope:**

- Testing on Latest Google Chrome browser
- Word Scrambling and validation logic
- Scoring and Hint deduction logic
- Reset Game and Leaderboard state management
- UI and Input validation (buttons, responsiveness, text input)
- User input error feedback and message display

**Out of Scope:**

- Cross-browser testing (e.g., Firefox, Safari, Edge)
- Performance testing under load
- Mobile device and Responsive design testing

### Tools & Resources
Tools
-GitHub issues for defect tracking
- Latest Chrome, Visual Studio Code
-Browser localstorage inpsection tools
-Screenshoot Capture Snipping tool
-Team Roles: Test Manager, Test Analyst, Test Executor

### Schedule

| Phase | Planned Duration | Actual Duration | Status |
|-------|------------------|-----------------|--------|
| | | | |
|Test planning and Design | 1 day | 1/2 day | Completed |
|Test case Development| 1 day| 1/2  day| Completed |
|Test Execution(Static and Manual)| 2 days| 1 day| Completed |
|Defect logging and Reporting| 1 day| 1/2 day| Completed |
Total  | 5 Days| 3.5 Days | Ahead of Schedule |
## Risk Analysis

### Risks

| ID | Feature | Risk Description | Likelihood | Impact | Priority | Mitigation Strategy |
|----|---------|------------------|------------|--------|----------|---------------------|
| R1 | Scoring System | Incorrect bonus calculation | High | High | Critical | Extensive boundary testing around puzzle counts |
| R2 | Leaderboard | Data loss when we reload or corruption in localStorage | Medium | High | High | Test if the scores will be lost across different browser sessions |
| R3 | Word Scrambling | Original word displayed instead of scrambled | Low | High | High | Test scrambling algorithm with various word lengths by clicking on new puzzle button |
| R4 | Input Validation | Game crashes with special character inputs | Medium | Medium | Medium | Implement comprehensive input sanitization |
| R5 | Hint System | Multiple hint charges for single use | Medium | Medium | Medium | Test hint flag reset mechanism |
| R6 | Reset Function | Incomplete state reset causing data leaks | Medium | High | High | Verify all variables reset to initial state |
| R7 | Accessibility | Poor accessibility compliance | High | Medium | Medium | Static analysis and screen reader testing |
| R8 | Code Maintainability | Poor code structure and practices | Medium | Medium | Medium | Code review and static analysis |


### Risk Coverage

- Tested Risks Percent: 100% (8/8)
- Untested Risks Percent: 0%

## Test Cases

| ID | Feature | Objective | Expected Result | Actual Result | Status | Risk Link |
|----|---------|-----------|----------------|---------------|--------|-----------|
| TC-01| Incorrect bonus calculation|Verify score doubles after 3rd puzzle | Score multiplied by 2 after 3 correct answers | Score correctly doubled to 60 | Passed | R1 |
| TC-02 | Leaderboard | Test top 3 score sorting |	Scores display in descending order | Scores properly sorted (60,20,10)|Passed |	R2 |
| TC-03| Reset Game | Verify complete state reset |	All scores and progress reset to 0 |Complete reset achieved	| Passed |	R6 |
| TC-04 | Word Scramble | Ensure scrambled word is not the original correct word | Different arrangement of letters | Words properly scrambled | Passed	| R3 |
| TC-05 | Hint System |	Test single hint charge per puzzle | 2 points deducted | Hint cost applied correctly | Passed | R5 |
| TC-06	| Input Validation | Test special character input |	Graceful error handling	| Input safely handled | Passed	| R4 |
| TC-07 | Scoring |	Verify hint-used scoring and score reduced to 5 points | Reduced points awarded with hint |	Correct scoring applied | Passed | R1 |
|TC-08 | UI Responsiveness | Test button functionality | All controls work as expected |	Interface responsive | Passed | N/A |
|TC-09 | Leaderboard Update | Test score persistence after refresh | Scores maintained after browser restart | Scores persisted correctly | Passed | R2 |
| TC-10 | Multiple Sessions	| Verify independent game sessions | No state leakage between plays	| Sessions isolated properly | Passed | R6 |
| TC-11 | Static Analysis |	Code quality and accessibility | No critical static analysis issues	| 2 medium severity issues found | Partial |	R7, R8 |
| TC-12 | Input Validation	| Verify alphabetic-only input | Non-alphabetic inputs rejected	| Accepts numbers and symbols |	Failed	| R4 |

## Defects

| ID | Issue Title | Severity | Risk ID | Status | GitHub Link |
|----|-------------|----------|---------|--------|-------------|
| D1 | Leaderboard stores intermediate scores | Medium | R2 | Open | https://github.com/PLP-Database-Design/wk-5-secbyteX03-1/issues/2 | 
| D2 | Hint button accessible when no hint available | Low | R5 | Open | https://github.com/PLP-Database-Design/wk-5-secbyteX03-1/issues/3 |
| D3 | ARIA role used instead of semantic HTML | Medium | R7 | Open | https://github.com/PLP-Database-Design/wk-5-secbyteX03-1/issues/4 |
| D4 | Accessibility role consistency issues | Medium | R7 | Open | https://github.com/PLP-Database-Design/wk-5-secbyteX03-1/issues/5 |
| D5 | Input field lacks alphabetic character validation | Medium | R4 | Open | https://github.com/PLP-Database-Design/wk-5-secbyteX03-1/issues/6 |


## Metrics

- Test Case Pass Percent: 100% (10/10 passed) - Dynamic Testing 
- Defect Density: : 0.5 (5 defects / 10 test cases)
- Risk Coverage Percent: 100%
- Static Analysis Defect Density: 2 issues identified by SonarQube
- Regression Success Rate: 100%

### Defect Summary

- Total Defects Logged: 5
- Critical High: 0
- Fix Rate: 0% - No fixes were made during these tests.

## Test Control & Project Management

### Phases

| Phase | Deliverable | Actual Output | Variance | Owner |
|-------|-------------|---------------|----------|-------|
| Planning | Test Strategy | Comprehensive test plan | None | Jackline |
| Analysis | Risk assessment | 8 prioritized risks | Added static analysis risks | Magret |
| Execution | Test results | 100% pass rate | Above 85% target | Gold |
| Static Analysis | Code quality report | 2 medium issues found | As expected | Team |
| Reporting | Defect log | 4 total issues | 2 dynamic + 2 static | Team |

**Progress Tracking Method**  : Daily online meetings, GitHub issue tracking, google docs.
**Change Control Notes** : Added static analysis phase after initial planning.

## Lessons Learned

- Most Defect Prone Feature: Code quality and accessibility compliance. 
- Risk Analysis Impact: Static analysis revealed important maintainability issues not caught in dynamic testing.
- Team Communication Effectiveness: High - integrated static testing findings effectively.
- Improvements for Next Cycle: 
 o	Include static analysis earlier in development cycle
o	Add automated accessibility testing tools
o	Implement code review process for accessibility compliance


## Attachments

**Image01** ![ Leaderboard ](/wk-5-secbyteX03-1/images/word-puzzle01.png "Leaderboard scores review")
**image02**: ![ Hint system ](/wk-5-secbyteX03-1/images/word-puzzle02.png "Hint feature should be diasbled once used ")
**image03:** ![ Code quality(Aria-role) ](/wk-5-secbyteX03-1/images/word-puzzle03.png "sonarqube code quality and accessibility")
**image04** : ![ Inconsistent use of semantic HTML ](/wk-5-secbyteX03-1/images/word-puzzle04.png "Semanatic HTML review")
**image05:** ![ Input validation ](/wk-5-secbyteX03-1/images/word-puzzle05.png "Input field should only accept alphabet")

- 

## Sign Off

| Name | Role | Initials | Date |
|------|------|-----------|------|
| Jackline Cherotich | Test Manager | JC | 28-10-2025 |
| Magret Faith | Risk Analyst | MF | 28-10-2025 |
| Amobigold Sikirat | Test Executor | GD | 28-10-2025 |

## Overall Summary

**Statement** : The Word Puzzle Game Plus application demonstrates good core functionality with working scoring mechanics and reliable features. During dynamic testing we only discovered minor usability issues, while during static analysis we identified important code quality and accessibility concerns by using SonarQube. The application functions well but requires code revisions and fixing for better accessibility compliance and maintainability before production release.


**Test Status:** [x] Completed / ☐ In Progress / ☐ Deferred



