# Smoke Test Cases - Saaed Mobile APP

## Overview
This smoke test suite contains **20 critical test cases** selected from the 99 optimized test cases. These tests cover the most essential functionalities to ensure the Saaed Mobile APP is stable and ready for further testing.

## Smoke Test Criteria
✅ App installation and launch  
✅ User authentication (login/register)  
✅ Core functionality (accident reporting)  
✅ Basic inquiry and search  
✅ Essential services access  
✅ Critical navigation  
✅ User session management  

---

## Installation & Launch

**SMOKE_TC_001: Verify mobile app installation and launch**
Steps:
1. Open App Store
2. Search for Saaed APP
3. Install the APP
4. Open the APP

Expected Result: Mobile app is installed and opens successfully

---

## Authentication

**SMOKE_TC_002: Verify user registration with valid credentials**
Steps:
1. Open Saaed APP
2. Click on Register
3. Fill all mandatory fields (Email, Mobile Number, Password)
4. Click on Register button
5. Enter OTP code
6. Click on Verify button

Expected Result: The user will register successfully

---

**SMOKE_TC_003: Verify user login with valid email address**
Steps:
1. Open Saaed APP
2. Click on Login
3. Enter valid email and password
4. Click on Login button

Expected Result: The user is logged in successfully

---

**SMOKE_TC_004: Verify user login with UAE PASS**
Steps:
1. Open Saaed APP
2. Click on Login
3. Click on "Login with UAE PASS" button
4. Enter Phone Number/Email/Emirates ID
5. Complete UAE PASS authentication

Expected Result: The user is able to login with UAE PASS successfully and UUID is linked to account

---

**SMOKE_TC_005: Verify that user cannot login with invalid credentials**
Steps:
1. Open Saaed APP
2. Click on Login
3. Enter invalid email/mobile and password
4. Click on Login button

Expected Result: Validation message should be displayed for wrong credentials

---

## Core Functionality - Accident Reporting

**SMOKE_TC_006: Verify anonymous user can report a traffic accident**
Steps:
1. Open Saaed APP
2. Click on "Report Traffic Accident" banner
3. Enter and verify mobile number
4. Answer initial questions (injuries, property damage, vehicle movable)
5. View location on map
6. Fill all mandatory data for accident details

Expected Result: The traffic accident report is created successfully with inquiry ID and notification sent

---

**SMOKE_TC_007: Verify logged-in user can report a traffic accident**
Steps:
1. Open Saaed APP and login
2. Click on "Report Traffic Accident" banner
3. Answer initial questions (injuries, property damage, vehicle movable)
4. View location on map
5. Fill all mandatory data for accident details

Expected Result: The traffic accident report is created successfully with inquiry ID and notification sent

---

**SMOKE_TC_008: Verify user can report accident type "حادث بين مركبات" (Between vehicles)**
Steps:
1. Open Saaed APP
2. Click on "Report Traffic Accident"
3. Enter and verify mobile number
4. Choose accident type "حادث بين مركبات"
5. Fill all mandatory data

Expected Result: Request is created successfully with inquiry ID and status marked as "طلب جديد"

---

**SMOKE_TC_009: Verify system behavior when user marks that there is injury**
Steps:
1. Open Saaed APP
2. Click on "Report Traffic Accident"
3. Answer "Yes" to question "هل يوجد إصابات؟"

Expected Result: User is redirected to page with 999 number asking to call emergency services

---

## Accident Report Inquiry

**SMOKE_TC_010: Verify anonymous user can inquiry about accident report from home screen**
Steps:
1. Open Saaed APP
2. Enter accident report number in the field below welcome message
3. Click on Inquiry icon
4. Enter the code

Expected Result: User can view the report current status

---

**SMOKE_TC_011: Verify logged-in user can inquiry about accident report from home screen**
Steps:
1. Open Saaed APP and login
2. Enter accident report number in the search field
3. Click on Search icon

Expected Result: User can view the report details and current status

---

**SMOKE_TC_012: Verify validation when searching for non-existent accident report number**
Steps:
1. Open Saaed APP
2. Enter an accident report number that doesn't exist in database
3. Click on Search icon

Expected Result: System displays message "Report Number is not Valid"

---

**SMOKE_TC_013: Verify user can download accident report**
Steps:
1. Open Saaed APP
2. Enter valid accident report number
3. Click on Inquiry icon
4. Enter the code
5. Click on View button
6. Download the report

Expected Result: User is able to download the report successfully

---

## Services & Navigation

**SMOKE_TC_014: Verify logged-in user can view services statistics**
Steps:
1. Open Saaed APP and login
2. Click on Services from navigation bar

Expected Result: User can view statistics including total accidents, TCN number, road assistance requests, and claims requests

---

**SMOKE_TC_015: Verify user can view all requests from My Requests section**
Steps:
1. Open Saaed APP and login
2. Click on Services
3. Click on My Requests

Expected Result: User can view all requests with Active and Closed status options

---

**SMOKE_TC_016: Verify user can request Saaed E-service from home screen banner**
Steps:
1. Open Saaed APP and login
2. Click on "Saaed E-Services" banner
3. Select a service
4. Fill all required fields
5. Click on Submit button

Expected Result: System redirects to Saaed E-services page and service is requested successfully

---

**SMOKE_TC_017: Verify user can request SAS from home screen banner/icon**
Steps:
1. Open Saaed APP and login
2. Click on "Saaed Auto Services" banner or icon
3. Fill all required fields
4. Click on Submit

Expected Result: System redirects to Saaed Auto Services page and service is requested successfully

---

## Profile & Settings

**SMOKE_TC_018: Verify user can view profile details**
Steps:
1. Open Saaed APP and login
2. Click on Profile icon from navigation bar

Expected Result: User can view profile details including email and TCN

---

**SMOKE_TC_019: Verify user can change language to Arabic**
Steps:
1. Open Saaed APP and login
2. Click on Change Language icon
3. Select "العربية"

Expected Result: Language is changed to Arabic successfully and all screens display in Arabic

---

## Session Management

**SMOKE_TC_020: Verify user can logout successfully**
Steps:
1. Open Saaed APP and login
2. Click on Profile from navigation bar
3. Click on Logout button
4. Click on Yes to confirm

Expected Result: User is logged out and redirected to home screen as anonymous user

---

## Summary

**Smoke Test Suite Overview:**
- **Total Smoke Tests:** 20
- **Source:** Selected from 99 optimized test cases
- **Coverage:**
  - Installation & Launch: 1 test
  - Authentication: 4 tests
  - Core Functionality (Accident Reporting): 4 tests
  - Accident Report Inquiry: 4 tests
  - Services & Navigation: 4 tests
  - Profile & Settings: 2 tests
  - Session Management: 1 test

**Purpose:**
These smoke tests ensure that:
1. The app can be installed and launched
2. Users can authenticate (register/login)
3. Core accident reporting functionality works
4. Users can search and inquiry about reports
5. Basic services are accessible
6. Navigation works correctly
7. User sessions are managed properly

**Execution Time:** Approximately 60-90 minutes

**Recommended Execution:**
- Before each major release
- After critical bug fixes
- After environment setup/changes
- Daily in CI/CD pipeline (automated)

---

*Generated from 99 optimized test cases on 2025-11-04*
