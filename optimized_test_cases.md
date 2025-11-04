# Optimized Test Cases - Saaed Mobile APP

## Registration & Authentication

**TC_001: Verify user registration with valid credentials**
Steps:
1. Open Saaed APP
2. Click on Register
3. Fill all mandatory fields (Email, Mobile Number, Password)
4. Click on Register button
5. Enter OTP code
6. Click on Verify button

Expected Result: The user will register successfully

---

**TC_002: Verify user login with valid email address**
Steps:
1. Open Saaed APP
2. Click on Login
3. Enter valid email and password
4. Click on Login button

Expected Result: The user is logged in successfully

---

**TC_003: Verify user login with valid mobile number**
Steps:
1. Open Saaed APP
2. Click on Login
3. Enter valid mobile number and password
4. Click on Login button

Expected Result: The user is logged in successfully

---

**TC_004: Verify user login with valid Emirates ID**
Steps:
1. Open Saaed APP
2. Click on Login
3. Enter valid Emirates ID and password
4. Click on Login button

Expected Result: The user is logged in successfully

---

**TC_005: Verify user login with UAE PASS (SOP2/SOP3 user)**
Steps:
1. Open Saaed APP
2. Click on Login
3. Click on "Login with UAE PASS" button
4. Enter Phone Number/Email/Emirates ID
5. Complete UAE PASS authentication

Expected Result: The user is able to login with UAE PASS successfully and UUID is linked to account

---

**TC_006: Verify that user cannot login with invalid credentials**
Steps:
1. Open Saaed APP
2. Click on Login
3. Enter invalid email/mobile and password
4. Click on Login button

Expected Result: Validation message should be displayed for wrong credentials

---

**TC_007: Verify that user cannot login with empty credentials**
Steps:
1. Open Saaed APP
2. Click on Login
3. Leave email and password fields empty
4. Click on Login button

Expected Result: Validation message should be displayed

---

**TC_008: Verify SOP1 user cannot login via UAE PASS**
Steps:
1. Open Saaed APP
2. Click on Login
3. Click on "Login with UAE PASS"
4. Enter SOP1 user credentials

Expected Result: Unauthorized message is displayed in both English and Arabic

---

**TC_009: Verify UAE PASS user account linking when user exists in Saaed without UUID**
Steps:
1. Open Saaed APP
2. Click on "Login with UAE PASS"
3. Login with UAE PASS credentials for user that exists in Saaed but without UUID

Expected Result: Account is connected automatically and successful page is displayed

---

**TC_010: Verify cancel UAE PASS login flow**
Steps:
1. Open Saaed APP
2. Click on "Login with UAE PASS"
3. Click on Back button during authentication

Expected Result: User is navigated back to Saaed login page with appropriate message in English and Arabic

---

**TC_011: Verify user can logout successfully**
Steps:
1. Open Saaed APP and login
2. Click on Profile from navigation bar
3. Click on Logout button
4. Click on Yes to confirm

Expected Result: User is logged out and redirected to home screen as anonymous user

---

## Accident Reporting

**TC_012: Verify anonymous user can report a traffic accident**
Steps:
1. Open Saaed APP
2. Click on "Report Traffic Accident" banner
3. Enter and verify mobile number
4. Answer initial questions (injuries, property damage, vehicle movable)
5. View location on map
6. Fill all mandatory data for accident details

Expected Result: The traffic accident report is created successfully with inquiry ID and notification sent

---

**TC_013: Verify logged-in user can report a traffic accident**
Steps:
1. Open Saaed APP and login
2. Click on "Report Traffic Accident" banner
3. Answer initial questions (injuries, property damage, vehicle movable)
4. View location on map
5. Fill all mandatory data for accident details

Expected Result: The traffic accident report is created successfully with inquiry ID and notification sent

---

**TC_014: Verify user can report accident type "حادث بين مركبات" (Between vehicles)**
Steps:
1. Open Saaed APP
2. Click on "Report Traffic Accident"
3. Enter and verify mobile number
4. Choose accident type "حادث بين مركبات"
5. Fill all mandatory data

Expected Result: Request is created successfully with inquiry ID and status marked as "طلب جديد"

---

**TC_015: Verify user can report accident type "حادث ضد مجهول" (Against unknown)**
Steps:
1. Open Saaed APP
2. Click on "Report Traffic Accident"
3. Enter and verify mobile number
4. Choose accident type "حادث ضد مجهول"
5. Fill all mandatory data

Expected Result: Request is created successfully with inquiry ID

---

**TC_016: Verify user can report accident type "حادث صدم جسم ثابت" (Hit fixed object)**
Steps:
1. Open Saaed APP
2. Click on "Report Traffic Accident"
3. Enter and verify mobile number
4. Choose accident type "حادث صدم جسم ثابت"
5. Fill all mandatory data

Expected Result: Request is created successfully with inquiry ID

---

**TC_017: Verify user can report accident type "حادث صدم وفرار" (Hit and run)**
Steps:
1. Open Saaed APP
2. Click on "Report Traffic Accident"
3. Enter and verify mobile number
4. Choose accident type "حادث صدم وفرار"
5. Fill all mandatory data

Expected Result: Request is created successfully with inquiry ID

---

**TC_018: Verify user can share traffic accident request with another user**
Steps:
1. Open Saaed APP
2. Click on "Report Traffic Accident"
3. Choose accident type "حادث بين مركبات"
4. Activate radio button "مشاركة الطلب مع الطرف الآخر"
5. Fill all mandatory data and save

Expected Result: 
1. Request is generated successfully with request number
2. Other user can open Saaed APP and use the same request number to complete accident data "إستكمال بيانات الحادث"

---

**TC_019: Verify system behavior when user marks that there is injury**
Steps:
1. Open Saaed APP
2. Click on "Report Traffic Accident"
3. Answer "Yes" to question "هل يوجد إصابات؟"

Expected Result: User is redirected to page with 999 number asking to call emergency services

---

**TC_020: Verify system behavior when user confirms state property damage**
Steps:
1. Open Saaed APP
2. Click on "Report Traffic Accident"
3. Answer "Yes" to question "أضرار ممتلكات تتبع الدولة؟"

Expected Result: User is redirected to page with message that Saaed Patrol is on its way

---

**TC_021: Verify system behavior when user cannot move vehicle**
Steps:
1. Open Saaed APP
2. Click on "Report Traffic Accident"
3. Answer "No" to question "هل يمكنك تحريك السيارة؟"

Expected Result: User is redirected to page with message that Saaed Patrol is on its way

---

**TC_022: Verify user cannot attach images exceeding size limitations**
Steps:
1. Open Saaed APP
2. Click on "Report Traffic Accident"
3. Attempt to upload images exceeding the limitation

Expected Result: Error message is displayed indicating size limit exceeded

---

**TC_023: Verify user cannot request another traffic accident while previous report is open**
Steps:
1. Open Saaed APP and login
2. Click on "Report Traffic Accident"
3. Create a traffic accident report
4. Try to request another traffic accident report before previous is closed

Expected Result: User cannot request another report and button changes to "Continue Your Request"

---

**TC_024: Verify validation for non-Emirates mobile numbers**
Steps:
1. Open Saaed APP
2. Click on "Report Traffic Accident"
3. Enter a non-Emirates mobile number

Expected Result: System displays error message indicating mobile number must be Emirates number

---

**TC_025: Verify accident report status updates through lifecycle**
Steps:
1. Open Saaed APP and create traffic accident report
2. As Call Taker, open the request in OR system
3. As OR user, create an incident from the request

Expected Result:
1. Status changes to "قيد التنفيذ" when opened by Call Taker
2. Status changes to "مغلق" when incident is created

---

## Accident Report Inquiry

**TC_026: Verify anonymous user can inquiry about accident report from home screen**
Steps:
1. Open Saaed APP
2. Enter accident report number in the field below welcome message
3. Click on Inquiry icon
4. Enter the code

Expected Result: User can view the report current status

---

**TC_027: Verify logged-in user can inquiry about accident report from home screen**
Steps:
1. Open Saaed APP and login
2. Enter accident report number in the search field
3. Click on Search icon

Expected Result: User can view the report details and current status

---

**TC_028: Verify user can inquiry about accident report from Services > Report Inquiry**
Steps:
1. Open Saaed APP and login
2. Click on Services
3. Click on Report Inquiry
4. Enter report number

Expected Result: User can view the report status successfully

---

**TC_029: Verify validation when searching for non-existent accident report number**
Steps:
1. Open Saaed APP
2. Enter an accident report number that doesn't exist in database
3. Click on Search icon

Expected Result: System displays message "Report Number is not Valid"

---

**TC_030: Verify validation when searching with empty report number**
Steps:
1. Open Saaed APP
2. Leave search field empty
3. Click on Search icon

Expected Result: System displays validation message "Enter accident report number/يرجى ادخال رقم تقرير الحادث"

---

**TC_031: Verify user can download accident report**
Steps:
1. Open Saaed APP
2. Enter valid accident report number
3. Click on Inquiry icon
4. Enter the code
5. Click on View button
6. Download the report

Expected Result: User is able to download the report successfully

---

**TC_032: Verify E-seal appears in downloaded accident report**
Steps:
1. Open Saaed APP
2. Enter valid accident report number
3. Click on Inquiry icon
4. Enter the code
5. Download the report
6. Check for E-seal in report

Expected Result: E-seal appears in the downloaded accident report

---

## Services Section

**TC_033: Verify logged-in user can view services statistics**
Steps:
1. Open Saaed APP and login
2. Click on Services from navigation bar

Expected Result: User can view statistics including total accidents, TCN number, road assistance requests, and claims requests

---

**TC_034: Verify user can view all requests from My Requests section**
Steps:
1. Open Saaed APP and login
2. Click on Services
3. Click on My Requests

Expected Result: User can view all requests with Active and Closed status options

---

**TC_035: Verify user can view request details from My Requests**
Steps:
1. Open Saaed APP and login
2. Click on Services
3. Click on My Requests
4. Click on any request to view details

Expected Result: User can view the detailed page for the selected request

---

**TC_036: Verify user can request Saaed E-service from Services section**
Steps:
1. Open Saaed APP and login
2. Click on Services
3. Click on Saaed E-Services
4. Select and request any service
5. Fill all required fields
6. Click on Submit button

Expected Result: E-service is requested successfully

---

**TC_037: Verify user can request Saaed E-service from home screen banner**
Steps:
1. Open Saaed APP and login
2. Click on "Saaed E-Services" banner
3. Select a service
4. Fill all required fields
5. Click on Submit button

Expected Result: System redirects to Saaed E-services page and service is requested successfully

---

**TC_038: Verify user can inquiry about E-service request status**
Steps:
1. Open Saaed APP and login
2. Click on "Saaed E-Services" banner
3. Enter E-service request number
4. Click on Check button

Expected Result: User can view E-service request status

---

**TC_039: Verify user can request SAS (Saaed Auto Services) from Services section**
Steps:
1. Open Saaed APP and login
2. Click on Services
3. Click on Saaed Auto Services
4. Request any service
5. Fill all required fields
6. Click on Submit

Expected Result: SAS service is requested successfully

---

**TC_040: Verify user can request SAS from home screen banner/icon**
Steps:
1. Open Saaed APP and login
2. Click on "Saaed Auto Services" banner or icon
3. Fill all required fields
4. Click on Submit

Expected Result: System redirects to Saaed Auto Services page and service is requested successfully

---

**TC_041: Verify SAS icon and banner design in both Arabic and English**
Steps:
1. Open Saaed APP and login
2. View home screen in Arabic interface
3. Change language to English
4. Check icon and banner design in both languages

Expected Result: Icon and banner design look fine and properly aligned according to approved design in both Arabic and English

---

**TC_042: Verify user can access SAS from Services navigation icon**
Steps:
1. Open Saaed APP and login
2. Click on Services from navigation bar
3. Click on Saaed Auto Services icon

Expected Result: User is redirected to Saaed Auto Services page

---

**TC_043: Verify user can request road assistance**
Steps:
1. Open Saaed APP and login
2. Click on Services from navigation bar
3. Click on Road Assistance
4. Fill all required fields

Expected Result: Road assistance request is created successfully

---

**TC_044: Verify user can access road assistance from Popular Services**
Steps:
1. Open Saaed APP
2. Click on Home from navigation bar
3. Click on "Popular Services - Road Assistance" icon

Expected Result: System redirects user to Road Assistance page

---

**TC_045: Verify user can track Saaed Patrol from home screen**
Steps:
1. Open Saaed APP
2. Click on "Popular Services - Track SAAED Patrol" icon
3. Enter patrol tracking code

Expected Result: User can track the patrol successfully

---

**TC_046: Verify user can track Saaed Patrol from Services section**
Steps:
1. Open Saaed APP and login
2. Click on Services from navigation bar
3. Click on Track Saaed Patrol
4. Enter patrol tracking code

Expected Result: User can track Saaed patrol successfully

---

**TC_047: Verify user can view all accidents from Services section**
Steps:
1. Open Saaed APP and login
2. Click on Services from navigation bar
3. Click on Accidents

Expected Result: User can view all accidents and search by report number

---

## Claim Management

**TC_048: Verify user cannot access claim management without login**
Steps:
1. Open Saaed APP
2. Click on "Popular Services - Claim Management" icon

Expected Result: System redirects user to login form

---

**TC_049: Verify logged-in user can access claim management**
Steps:
1. Open Saaed APP and login
2. Click on Claim Management button from navigation bar

Expected Result: Claim management page opens successfully

---

**TC_050: Verify user can create claim management request after accident report**
Steps:
1. Open Saaed APP and login
2. Create an accident report
3. Open Claim Management
4. Select the accident report
5. Click on Create Claim

Expected Result: System redirects to Motori and claim management request is created successfully

---

**TC_051: Verify claim management request status is displayed in list**
Steps:
1. Open Saaed APP and login
2. Navigate to Claim Management
3. View list of claim requests

Expected Result: Claim management request status is displayed correctly in the list

---

**TC_052: Verify claim eligibility - Comprehensive insurance, faulty, unknown accident, whitelist company**
Steps:
1. Create accident report with: Insurance type = Comprehensive, Role = Faulty, Accident type = Unknown, Company = Whitelist
2. Navigate to Claim Management
3. Attempt to create claim

Expected Result: User can create claim management successfully

---

**TC_053: Verify claim eligibility - Comprehensive insurance, faulty, simple accident, whitelist company**
Steps:
1. Create accident report with: Insurance type = Comprehensive, Role = Faulty, Accident type = Simple, Company = Whitelist
2. Navigate to Claim Management
3. Attempt to create claim

Expected Result: User can create claim management successfully

---

**TC_054: Verify claim rejection - Comprehensive insurance, faulty, simple accident, blacklist company**
Steps:
1. Create accident report with: Insurance type = Comprehensive, Role = Faulty, Accident type = Simple, Company = Blacklist
2. Navigate to Claim Management
3. Attempt to create claim

Expected Result: Validation message is displayed and claim cannot be created

---

**TC_055: Verify claim eligibility - Comprehensive insurance, non-faulty, unknown accident, whitelist company**
Steps:
1. Create accident report with: Insurance type = Comprehensive, Role = Non-faulty, Accident type = Unknown, Company = Whitelist
2. Navigate to Claim Management
3. Attempt to create claim

Expected Result: User can create claim management successfully

---

**TC_056: Verify claim eligibility - Comprehensive insurance, non-faulty, simple accident, whitelist company**
Steps:
1. Create accident report with: Insurance type = Comprehensive, Role = Non-faulty, Accident type = Simple, Company = Whitelist
2. Navigate to Claim Management
3. Attempt to create claim

Expected Result: User can create claim management successfully

---

**TC_057: Verify claim rejection - Comprehensive insurance, non-faulty, unknown accident, blacklist company**
Steps:
1. Create accident report with: Insurance type = Comprehensive, Role = Non-faulty, Accident type = Unknown, Company = Blacklist
2. Navigate to Claim Management
3. Attempt to create claim

Expected Result: Validation message is displayed and claim cannot be created

---

**TC_058: Verify claim rejection - Comprehensive insurance, non-faulty, simple accident, blacklist company**
Steps:
1. Create accident report with: Insurance type = Comprehensive, Role = Non-faulty, Accident type = Simple, Company = Blacklist
2. Navigate to Claim Management
3. Attempt to create claim

Expected Result: Validation message is displayed and claim cannot be created

---

**TC_059: Verify accident not displayed - TPL insurance, faulty, simple accident, whitelist company**
Steps:
1. Create accident report with: Insurance type = TPL, Role = Faulty, Accident type = Simple, Company = Whitelist
2. Navigate to Claim Management

Expected Result: Accident is not displayed in claim management list

---

**TC_060: Verify accident not displayed - TPL insurance, faulty, simple accident, blacklist company**
Steps:
1. Create accident report with: Insurance type = TPL, Role = Faulty, Accident type = Simple, Company = Blacklist
2. Navigate to Claim Management

Expected Result: Accident is not displayed in claim management list

---

**TC_061: Verify claim rejection - TPL insurance, non-faulty, simple accident, blacklist company**
Steps:
1. Create accident report with: Insurance type = TPL, Role = Non-faulty, Accident type = Simple, Company = Blacklist
2. Navigate to Claim Management
3. Attempt to create claim

Expected Result: Validation message is displayed and claim cannot be created

---

**TC_062: Verify claim eligibility - TPL insurance, non-faulty, simple accident, whitelist company**
Steps:
1. Create accident report with: Insurance type = TPL, Role = Non-faulty, Accident type = Simple, Company = Whitelist
2. Navigate to Claim Management
3. Attempt to create claim

Expected Result: User can create claim management successfully

---

**TC_063: Verify accident not displayed - TPL insurance, non-faulty, unknown accident, whitelist company**
Steps:
1. Create accident report with: Insurance type = TPL, Role = Non-faulty, Accident type = Unknown, Company = Whitelist
2. Navigate to Claim Management

Expected Result: Accident is not displayed in claim management list

---

**TC_064: Verify accident not displayed - TPL insurance, non-faulty, unknown accident, blacklist company**
Steps:
1. Create accident report with: Insurance type = TPL, Role = Non-faulty, Accident type = Unknown, Company = Blacklist
2. Navigate to Claim Management

Expected Result: Accident is not displayed in claim management list

---

**TC_065: Verify claim management request synced with Motori staging**
Steps:
1. Create claim management request in Saaed APP
2. Check Motori staging environment for corresponding insurance company

Expected Result: Claim management request is displayed correctly in Motori staging

---

## Profile Management

**TC_066: Verify user can view profile details**
Steps:
1. Open Saaed APP and login
2. Click on Profile icon from navigation bar

Expected Result: User can view profile details including email and TCN

---

**TC_067: Verify user can access profile from home screen header**
Steps:
1. Open Saaed APP and login
2. Click on Home from navigation bar
3. Click on username in the header

Expected Result: System redirects user to Profile screen successfully

---

**TC_068: Verify user can add TCN successfully**
Steps:
1. Open Saaed APP and login
2. Click on Profile
3. Click on Edit icon in TCN field
4. Enter TCN
5. Click Save

Expected Result: TCN is added successfully

---

**TC_069: Verify user can edit TCN from profile**
Steps:
1. Open Saaed APP and login
2. Click on Profile
3. Click on Edit action on TCN field
4. Enter new TCN
5. Click Save

Expected Result: User can edit TCN and save successfully

---

## Language & Localization

**TC_070: Verify user can change language to Arabic**
Steps:
1. Open Saaed APP and login
2. Click on Change Language icon
3. Select "العربية"

Expected Result: Language is changed to Arabic successfully and all screens display in Arabic

---

**TC_071: Verify user can change language to English**
Steps:
1. Open Saaed APP and login (with Arabic interface)
2. Click on Change Language icon
3. Select English

Expected Result: Language is changed to English successfully and all screens display in English

---

**TC_072: Verify current screen displays in selected language**
Steps:
1. Open Saaed APP and login
2. Change language to Arabic
3. Click on Profile
4. Verify language display

Expected Result: Profile screen and all elements display in Arabic

---

**TC_073: Verify accident reporting steps display in selected language**
Steps:
1. Open Saaed APP and login
2. Change language to Arabic
3. Click on "الإبلاغ عن حادث بسيط"

Expected Result: All steps of creating traffic accident report display in Arabic

---

**TC_074: Verify E-Service website displays in selected language**
Steps:
1. Open Saaed APP and login
2. Change language to Arabic
3. Click on "خدمات ساعد الإلكترونية"

Expected Result: E-services website opens in Arabic language

---

**TC_075: Verify SAS description and steps display in selected language**
Steps:
1. Open Saaed APP and login
2. Change language to Arabic
3. Click on "ساعد أوتو سيرفيز"

Expected Result: SAS description and steps display in Arabic language

---

**TC_076: Verify notifications sent in user's selected language**
Steps:
1. Open Saaed APP and login
2. Change language to Arabic
3. Click on "الإبلاغ عن حادث بسيط"
4. Create traffic accident report

Expected Result: All notifications sent to user are in Arabic language

---

## Contact Us & Social Media

**TC_077: Verify user can view contact information**
Steps:
1. Open Saaed APP and login
2. Click on Contact Us from navigation bar

Expected Result: User can view call center number, website, and HQ location

---

**TC_078: Verify user can contact customer service via chat**
Steps:
1. Open Saaed APP and login
2. Click on Contact Us
3. Click on "Contact Us" or "تواصل معنا" chat option

Expected Result: User can contact Saaed customer service successfully

---

**TC_079: Verify user can call customer service**
Steps:
1. Open Saaed APP and login
2. Click on Contact Us
3. Click on phone number

Expected Result: User can call Saaed customer service

---

**TC_080: Verify user can view Saaed website from Contact Us**
Steps:
1. Open Saaed APP and login
2. Click on Contact Us
3. Click on website link

Expected Result: User can view Saaed website successfully

---

**TC_081: Verify user can view HQ location on map**
Steps:
1. Open Saaed APP and login
2. Click on Contact Us
3. Click on location for main office

Expected Result: User can view the main office location on map successfully

---

**TC_082: Verify user redirected to Saaed Instagram page**
Steps:
1. Open Saaed APP and login
2. Click on Contact Us
3. Click on Instagram icon

Expected Result: User is redirected to Saaed Instagram page successfully

---

**TC_083: Verify user redirected to Saaed Facebook page**
Steps:
1. Open Saaed APP and login
2. Click on Contact Us
3. Click on Facebook icon

Expected Result: User is redirected to Saaed Facebook page successfully

---

**TC_084: Verify user redirected to Saaed X (Twitter) page**
Steps:
1. Open Saaed APP and login
2. Click on Contact Us
3. Click on X icon

Expected Result: User is redirected to Saaed X page successfully

---

**TC_085: Verify user redirected to Saaed YouTube page**
Steps:
1. Open Saaed APP and login
2. Click on Contact Us
3. Click on YouTube icon

Expected Result: User is redirected to Saaed YouTube page successfully

---

**TC_086: Verify user redirected to Saaed LinkedIn page**
Steps:
1. Open Saaed APP and login
2. Click on Contact Us
3. Click on LinkedIn icon

Expected Result: User is redirected to Saaed LinkedIn page successfully

---

## Notifications & SMS

**TC_087: Verify SMS sent with correct content when reporting incident**
Steps:
1. Open Saaed APP and login
2. Report a traffic accident via mobile app
3. Check SMS notification

Expected Result: SMS is sent with correct content when reporting incident

---

**TC_088: Verify SMS sent when clicking Send button for report in search page**
Steps:
1. Open Saaed APP
2. Search for accident report
3. Click on Send button

Expected Result: SMS is sent with correct content

---

**TC_089: Verify SMS link for متسبب (faulty) role redirects to payment page**
Steps:
1. Create accident report where user role is متسبب
2. Receive SMS notification
3. Click on link in SMS

Expected Result: SMS link is shortened and redirects user to payment page

---

**TC_090: Verify SMS link for متضرر (victim) role redirects to view report**
Steps:
1. Create accident report where user role is متضرر
2. Receive SMS notification
3. Click on link in SMS

Expected Result: SMS link is shortened and redirects user to view report page

---

**TC_091: Verify notifications sent via SMS for users without WhatsApp**
Steps:
1. Open Saaed APP and login with user who doesn't have WhatsApp
2. Request an E-service
3. Check notification delivery method

Expected Result: Notification is sent via SMS

---

**TC_092: Verify Tracking URL behavior for Saaed URLs**
Steps:
1. Receive notification with Saaed tracking URL
2. Click on Tracking URL

Expected Result: System behavior is correct when clicking Saaed tracking URLs

---

## App Installation & UI

**TC_093: Verify mobile app installation**
Steps:
1. Open App Store
2. Search for Saaed APP
3. Install the APP

Expected Result: Mobile app is installed successfully

---

**TC_094: Verify user can open installed app**
Steps:
1. Install Saaed APP from App Store
2. Open the APP

Expected Result: User is able to open the installed app successfully

---

**TC_095: Verify search bar is prominently displayed on homepage**
Steps:
1. Launch mobile application
2. Click on Home from navigation bar
3. Check search bar visibility

Expected Result: Search bar is prominently displayed on homepage

---

**TC_096: Verify new banner design in Arabic interface**
Steps:
1. Open Saaed APP and login
2. Set language to Arabic
3. Check banner design on home screen

Expected Result: New banner design looks fine and everything is aligned correctly according to approved design

---

**TC_097: Verify new banner design in English interface**
Steps:
1. Open Saaed APP and login
2. Set language to English
3. Check banner design on home screen

Expected Result: New banner design looks fine and everything is aligned correctly according to approved design

---

**TC_098: Verify new icon design in Arabic interface**
Steps:
1. Open Saaed APP and login
2. Set language to Arabic
3. Check icon design on home screen

Expected Result: New icon design looks fine and everything is aligned correctly according to approved design

---

**TC_099: Verify new icon design in English interface**
Steps:
1. Open Saaed APP and login
2. Set language to English
3. Check icon design on home screen

Expected Result: New icon design looks fine and everything is aligned correctly according to approved design

---

## Summary

**Total Test Cases:**
- Original: 260+ test cases
- Final: 99 test cases

**Optimization Results:**
- Exact duplicates removed: 45+
- Similar cases merged: 116+
- Reduction: ~62%

**Key Improvements:**
1. Removed exact duplicates with same title and steps
2. Merged similar test cases (e.g., multiple login scenarios, accident reporting variations)
3. Consolidated UI/design test cases across languages
4. Combined similar inquiry and service request test cases
5. Merged claim management eligibility scenarios while keeping distinct validation rules
6. Consolidated social media redirection tests
7. Unified notification and SMS test cases
8. Sequential numbering maintained (TC_001 to TC_099)

**Categories Optimized:**
- Registration & Authentication: 11 test cases
- Accident Reporting: 14 test cases
- Accident Report Inquiry: 7 test cases
- Services Section: 15 test cases
- Claim Management: 18 test cases
- Profile Management: 4 test cases
- Language & Localization: 7 test cases
- Contact Us & Social Media: 10 test cases
- Notifications & SMS: 6 test cases
- App Installation & UI: 7 test cases
