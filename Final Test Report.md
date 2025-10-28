# 🧪 Final Group Test Report Template — Word Puzzle Game Plus

**Level:** Intermediate QA | **Week 5:** Test Management

**Course:** Software Testing & Quality Assurance  
**Module:** Test Management (Week 5)  
**Project Type:** Group Assessment  
**Submission Date:** 2025-10-28

## Team Information

| Role | Name | Responsibilities |
|------|------|------------------|
| Test Manager | | Planning, scheduling, coordination, metric tracking |
| Risk Analyst | Magret Faith| Risk identification, prioritization, test design linkage |
| Test Executor | | Execution, evidence capture, defect logging |

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
| Reset Game | Clears score and progress instantly | |
| Leaderboard | Stores top 3 scores in localStorage | |
| Bonus Round | Every 3 puzzles → doubles score | |

## Test Plan

### Objectives
-Validate Leaderboard functionality that it displays top scores  and data persists
-Verify core game functionality — word scrambling, bonus calculations, and reset behavior.
-Confirm negative test cases (invalid input, no word entered,) are handled gracefully.
-Evaluate UI responsiveness across various screen sizes and environments.
-To apply risk based testing to prioritize high impact areas.
- To document identified defects and provide evidence

### Scope

**In Scope:**
-Testing on Latest Google Chrome browser 
-Word Scrambling and validation logic.
-Scoring and Hint deduction logic.
-Reset Game and Leaderboard state management.
-UI and Input validation like buttons, responsiveness, text input.
-User input error feedback and message display

**Out of Scope:**
-Cross-browser testing (e.g., Firefox, Safari, Edge).
-Performance testing under load.
-Mobile device and Responsive design testing

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
|Test planning and Design | 1 day | 1/2 day |Completed |
|Test case Development| 1 day| 1/2  day|Completed|
|Test Execution(Static and Manual)| 2 days| 1 day|Completed|
|Defect logging and Reporting| 1 day| 1/2 day|Completed|
Total  | 5 Days| 3.5 Days | Ahead of Schedule
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
| TC-02 | Leaderboard | TC-02	Leaderboard	Test top 3 score sorting |	Scores display in descending order	Scores properly sorted (60,20,10)|Passed	R2 |
| TC-03| Reset Game | Verify complete state reset |	All scores and progress reset to 0 |Complete reset achieved	| Passed |	R6 |
| TC-04 | Word Scramble | Ensure scrambled word is not the original correct word | Different arrangement of letters | Words properly scrambled | Passed	| R3 |
| TC-05 | Hint System |	Test single hint charge per puzzle |	2 points deducted |	Hint cost applied correctly |	Passed 	| R5 |
| TC-06	| Input Validation | Test special character input |	Graceful error handling	| Input safely handled | Passed	| R4 |
| TC-07 | Scoring |	Verify hint-used scoring and score reduced to 5 points | Reduced points awarded with hint |	Correct scoring applied | Passed | R1 |
|TC-08 | UI Responsiveness | 	Test button functionality | All controls work as expected |	Interface responsive |	Passed	|N/A |
|TC-09 |	Leaderboard Update	Test score persistence after refresh |	Scores maintained after browser restart	|Scores persisted correctly	| Passed |	R2 |
| TC-10 | Multiple Sessions	| Verify independent game sessions | No state leakage between plays	| Sessions isolated properly |	Passed | R6 |
| TC-11 | Static Analysis |	Code quality and accessibility | No critical static analysis issues	| 2 medium severity issues found | Partial |	R7, R8 |
| TC-12 | Input Validation	| Verify alphabetic-only input |	Non-alphabetic inputs rejected	| Accepts numbers and symbols |	Failed	| R4 |

## Defects

| ID | Issue Title | Severity | Risk ID | Status | GitHub Link |
|----|-------------|----------|---------|--------|-------------|
| D1 | Leaderboard stores intermediate scores | Medium | R2 | Open | Issue #1| 
| D2 | Hint button accessible when no hint available | Low | R5 | Open | Issue #2 |
| D3 | ARIA role used instead of semantic HTML | Medium | R7 | Open | Issue #3 |
| D4 | Accessibility role consistency issues | Medium | R7 | Open | Issue #4 |
| D5 | Input field lacks alphabetic character validation | Medium | R4 | Open | Issue#5 |


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

- 

## Sign Off

| Name | Role | Initials | Date |
|------|------|-----------|------|
| Jackline Cherotich | Test Manager | JC | 27-10-2025 |
| Magret Faith | Risk Analyst | MF | 10/28/2025 |
| | Amobigold Sikirat |Test executor |GD | 28-10-2025

## Overall Summary

**Statement** : The Word Puzzle Game Plus application demonstrates good core functionality with working scoring mechanics and reliable features. During dynamic testing we only discovered minor usability issues, while during static analysis we identified important code quality and accessibility concerns by using SonarQube. The application functions well but requires code revisions and fixing for better accessibility compliance and maintainability before production release.


**Test Status:** **Completed** / ☐ In Progress / ☐ Deferred

## Github Issues

## Default 1

**DEF-001:** Leaderboard stores intermediate cumulative scores. 
**Risk Link:** R2
**Feature:**Leaderboard
**Description**
The leaderboard cumulative scores are saved to localStorage, not final session scores.

**Steps to Reproduce**
1.	Play first puzzle, solve it and you get to Score 10 and this is saved to leaderboard and displayed.
2.	Play second puzzle, solve it and you will get the score of  20 and also this is saved to leaderboard and replaces the position of the score  10.
3.	Play third puzzle, this will trigger a bonus Score and you get double so the score will be  60 also saved to leaderboard and replaces the position for the score 20.
4.	Open DevTools then click Application  then localStorage then  view the leaderboard key.
**Expected Result**
Here the design decision was needed since our group had two possible interpretations in mind:
•	Option A: Leaderboard tracks best cumulative score achieved in a single continuous session
•	Option B: Leaderboard tracks final score when player explicitly ends session for example by having a finish game button
**Actual Result**
Leaderboard saves score after each puzzle solve, so it always reflects current cumulative score.
**Impact**
•	If player resets mid-session, their intermediate score is preserved in leaderboard
•	 There is no way to distinguish final session score from best cumulative score during session
•	User expectation unclear, the user will not be able to understand if  this a high score tracker or session completion tracker
Severity Justification: Medium - Functional but may not match design intent
**Recommendation**
1.	Clarify specification: What should leaderboard represent?
2.	If session-based: Add finish game button that saves final score only
3.	If cumulative: Keep current behavior but update README to document this explicitly
4.	Consider adding session timestamp to distinguish different play sessions

**Image01** ![ Leaderboard ](/wk-5-secbyteX03-1/images/word-puzzle01.png "Leaderboard scores review")


## Defect 2

**DEF-002:** Hint button accessible when no hint available
**Risk Link:** R5
**Feature:**  Hint System
**Description**
The hint button remains enabled and clickable even after a hint has already been used for the current puzzle, providing confusing user feedback when no additional hint is available.
**Steps to Reproduce**
1.	Start a new puzzle
2.	Click on the hint button and a hint is displayed and 2 points deducted
3.	Click on the hint button again and the error message appears
4.	Observe that button remains enabled throughout
**Expected Result:**
Hint button should be disabled or show visual feedback after being used to prevent user confusion about available actions.
**Actual Result**
Button remains fully enabled, requiring user to read error message to understand why second click doesn't work
**Impact:**
•	Minor user experience issue
•	Potential confusion about game mechanics
•	Inconsistent UI feedback
**Severity Justification:** Low - Cosmetic UI issue that doesn't affect functionality
**Recommendation:**
1.	Disable hint button after first use per puzzle
2.	Change button styling to indicate inactive state when all hints are used
3.	Re-enable button when new puzzle loads
4.	Add an explaining hint limitation

**image02**: ![ Hint system ](/wk-5-secbyteX03-1/images/word-puzzle02.png "Hint feature should be diasbled once used ")

## Defect 3

**DEF-003:** ARIA role used instead of semantic HTML 
**Risk Link:** R7
**Feature:** Code quality and accessibility
**Description:**
SonarQube static analysis detected use of ARIA roles on generic elements where semantic HTML tags would be more appropriate. This affects the accessibility, maintainability and code quality.
**Steps to reproduce:**
•	Open the index.html file in a Vs code and ensure you have sonarQube extension installed
•	Open the terminal and head over to sonarQube to view the issues
•	Double click on the issue listed to read more details
**Expected Result:**
Use semantic HTML elements (button, section, main, etc.) instead of generic elements with ARIA roles for better accessibility and code maintainability.
**Actual Result:**
Generic div elements with ARIA roles used throughout the codebase.
**Impact:**
•	Reduced accessibility support across different browsers and assistive technologies
•	Poor code maintainability and readability
•	Increased complexity requiring additional JavaScript for built-in behaviors
•	Potential SEO impact due to poor semantic structure
**Severity Justification:** Medium - Accessibility and maintainability concern that doesn't break functionality but impacts code quality
**Recommendation:**
1.	Replace <div role="button"> with actual <button> elements
2.	Use <main>, <section>, <nav> instead of <div role="main">
3.	Remove redundant ARIA roles when semantic elements provide the same meaning
4.	Conduct accessibility audit with screen readers to verify improvements
**image03:** ![ Code quality(Aria-role) ](/wk-5-secbyteX03-1/images/word-puzzle03.png "sonarqube code quality and accessibility")


## Defect 4

**DEF-004:** Accessibility role consistency issues 
**Risk Link:** R7
**Feature:** Code quality and accessibility
**Description:**
SonarQube analysis identified inconsistent use of ARIA roles and semantic HTML throughout the codebase. Some elements use proper semantic tags while others use generic elements with ARIA roles, creating maintenance challenges and potential accessibility gaps.
**Steps to reproduce**
•	open the index.html file in a Vs code and ensure you have sonarQube extension installed
•	Open the terminal and head over to sonarQube to view the issues
•	Double click on the issue listed to read more details
**Expected Result**
Consistent use of semantic HTML elements throughout the application with ARIA roles only used when no suitable semantic element exists.
**Actual Result**
Inconsistent implementation with some elements using semantic HTML and others using ARIA roles on generic elements.
**Impact**
•	Inconsistent user experience for assistive technology users
•	Higher maintenance costs due to mixed patterns
•	Potential accessibility compliance issues
•	Learning curve for new developers working on the codebase
**Severity Justification:** Medium - Code quality and accessibility issue that impacts maintainability and user experience
**Recommendation**
1.	Establish and follow consistent accessibility patterns
2.	Create accessibility guidelines for the project
3.	Replace all generic elements with ARIA roles where semantic alternatives exist
4.	Use ARIA roles only when no semantic HTML element can provide the required semantics
5.	Implement automated accessibility testing in CI/CD pipeline
**image04** : ![ Inconsistent use of semantic HTML ](/wk-5-secbyteX03-1/images/word-puzzle04.png "Semanatic HTML review")

## Defect 5

**DEF-005:** Input Field Lacks Alphabetic Character Validation 
**Risk Link:** R4
**Feature:** Input Validation
**Description:**
The input field accepts numeric characters and special symbols as valid guesses for scrambled words, which are always composed of alphabetic characters only. This lack of input filtering creates a poor user experience and allows invalid inputs that can never match the target word.
**Steps to Reproduce:**
1.	Start a new puzzle with scrambled word 
2.	Enter numeric characters in guess field for example 12345678
3.	Click Submit or press Enter
4.	Observe the application processes the numeric input as a valid guess attempt
5.	Repeat with special characters like !@#$%
6.	Repeat with mixed alphanumeric like abc123
**Expected Result**
•	Input field should reject or filter non-alphabetic characters
•	Show validation error message for invalid character inputs
•	Only accept letters A-Z (case insensitive)
**Actual Result**
•	Input field accepts any keyboard input including numbers and symbols
•	No client-side validation prevents invalid character submissions
•	System processes clearly invalid guesses, providing "Incorrect" feedback instead of proper validation messages
**Impact**
•	Poor user experience - users can waste attempts on obviously invalid inputs
•	No guidance for users about expected input format
•	Increased error rate due to accidental numeric/symbol input
•	Accessibility concern - no clear input requirements communicated
**Severity Justification:** Medium - Functional issue that impacts user experience and input validation integrity

**image05:** ![ Input validation ](/wk-5-secbyteX03-1/images/word-puzzle05.png "Input field should only accept alphabet")