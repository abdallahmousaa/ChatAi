# Saaed Mobile APP - Optimized Test Cases

## Overview
This repository contains optimized and deduplicated test cases for the Saaed Mobile APP, including a dedicated smoke test suite for critical functionality validation.

## Files

### 🔥 Smoke Test Suite

#### 1. **Smoke_Test_Cases.xlsx** (Critical Tests)
- **Format:** Excel (.xlsx)
- **Total Test Cases:** 20 critical smoke tests
- **Columns:**
  - TC ID (SMOKE_TC_001 to SMOKE_TC_020)
  - Test Case Description
  - Test Case Steps
  - Expected Result
- **Features:**
  - Red header row (indicates smoke tests)
  - Frozen header row
  - Auto-wrapped text
  - Optimized for quick execution
- **Execution Time:** 60-90 minutes
- **Purpose:** Verify critical functionality before detailed testing

#### 2. **smoke_test_cases.csv**
- CSV version of smoke tests
- Can be opened in Excel or any spreadsheet application

#### 3. **smoke_test_cases.md**
- Markdown version with detailed smoke test documentation
- Includes execution recommendations and coverage analysis

### 📋 Full Test Suite

### 1. **Optimized_Test_Cases.xlsx** (Primary Output)
- **Format:** Excel (.xlsx)
- **Columns:**
  - TC ID
  - Test Case Description
  - Test Case Steps
  - Expected Result
- **Total Test Cases:** 99
- **Features:**
  - Formatted headers with blue background
  - Frozen header row for easy scrolling
  - Auto-wrapped text in cells
  - Optimized column widths

### 2. **optimized_test_cases.csv**
- **Format:** CSV (Comma-Separated Values)
- Same content as Excel file, can be opened in Excel or any spreadsheet application
- UTF-8 encoding with BOM for proper character display

### 3. **optimized_test_cases.md**
- **Format:** Markdown
- Human-readable version with detailed summary
- Organized by categories

## Optimization Summary

### Test Case Count
- **Original:** 260+ test cases
- **Final:** 99 test cases
- **Reduction:** ~62%

### Actions Performed
- **Exact duplicates removed:** 45+
- **Similar cases merged:** 116+

### Test Categories (99 Test Cases)
1. **Registration & Authentication** - 11 TCs
2. **Accident Reporting** - 14 TCs
3. **Accident Report Inquiry** - 7 TCs
4. **Services Section** - 15 TCs
5. **Claim Management** - 18 TCs
6. **Profile Management** - 4 TCs
7. **Language & Localization** - 7 TCs
8. **Contact Us & Social Media** - 10 TCs
9. **Notifications & SMS** - 6 TCs
10. **App Installation & UI** - 7 TCs

## Key Improvements
✅ Removed all exact duplicates  
✅ Merged near-duplicates with same purpose  
✅ Kept most complete and well-written versions  
✅ Sequential numbering (TC_001 to TC_099)  
✅ Consistent format and structure  
✅ Clear categorization for easy navigation  
✅ Preserved all unique test scenarios

## Smoke Test Coverage

The smoke test suite covers:
- ✅ **Installation & Launch:** 1 test
- ✅ **Authentication:** 4 tests (register, login, UAE PASS, validation)
- ✅ **Core Functionality:** 4 tests (accident reporting, injury handling)
- ✅ **Accident Inquiry:** 4 tests (search, download, validation)
- ✅ **Services & Navigation:** 4 tests (statistics, requests, E-services, SAS)
- ✅ **Profile & Settings:** 2 tests (view profile, language change)
- ✅ **Session Management:** 1 test (logout)

## How to Use

### For Smoke Testing (Quick Validation)
1. Open **Smoke_Test_Cases.xlsx**
2. Execute all 20 tests in sequence (60-90 minutes)
3. Run before each release or after critical changes
4. All tests must pass before proceeding to full test suite

### For Full Testing (Comprehensive)
1. Open **Optimized_Test_Cases.xlsx** in Microsoft Excel, Google Sheets, or any spreadsheet application
2. Use filters on the header row to find specific test cases
3. Each test case has a unique ID (TC_001 to TC_099) for easy reference
4. Steps and expected results are clearly formatted for test execution

## Recommended Testing Strategy
1. **Run Smoke Tests First:** Execute all 20 smoke tests to validate critical functionality
2. **If Smoke Tests Pass:** Proceed with full test suite (99 tests)
3. **If Smoke Tests Fail:** Fix critical issues before continuing detailed testing
4. **Automation:** Consider automating smoke tests for CI/CD pipeline

---

*Generated on 2025-11-04*
