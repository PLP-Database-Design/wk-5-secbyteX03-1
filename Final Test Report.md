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

- 

### Scope

**In Scope:**
- 

**Out of Scope:**
- 

### Tools & Resources

- 

### Schedule

| Phase | Planned Duration | Actual Duration | Status |
|-------|------------------|-----------------|--------|
| | | | |

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
| | Test Manager | | |
|Magret Faith | Risk Analyst |MF | 10/28/2025|
| | Test Executor | | |

## Overall Summary

**Statement:** 

**Test Status:** ☐ Completed / ☐ In Progress / ☐ Deferred
