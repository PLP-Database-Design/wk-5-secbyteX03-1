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
| | | | | | | |

## Defects

| ID | Issue Title | Severity | Risk ID | Status | GitHub Link |
|----|-------------|----------|---------|--------|-------------|
| | | | | | |

## Metrics

- Test Case Pass Percent: 
- Defect Density: 
- Risk Coverage Percent: 
- Regression Success Rate: 

### Defect Summary

- Total Defects Logged: 
- Critical High: 
- Fix Rate: 

## Test Control & Project Management

### Phases

| Phase | Deliverable | Actual Output | Variance | Owner |
|-------|-------------|---------------|----------|-------|
| | | | | |

**Progress Tracking Method:**  
**Change Control Notes:**

## Lessons Learned

- Most Defect Prone Feature: 
- Risk Analysis Impact: 
- Team Communication Effectiveness: 
- Improvements for Next Cycle: 

## Attachments

- 

## Sign Off

| Name | Role | Initials | Date |
|------|------|-----------|------|
| Jackline Cherotich | Test Manager | JC | 28-10-2025 |
| Magret Faith | Risk Analyst | MF |28-10-2025 |
| | Test Executor | | |

## Overall Summary

**Statement:** 

**Test Status:** ☐ Completed / ☐ In Progress / ☐ Deferred
