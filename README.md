## 📚 Sections
<h4 align="left"><a href="https://github.com/caroolps/QA-AS2-Group">INÍCIO</a></h4>
<h4 align="left"><a href="https://github.com/caroolps/AUTOMATIZADO/blob/main/README.md">TESTES AUTOMATIZADOS</a></h4>


## 📋 Test Plan

This test plan outlines the scenarios and conditions to be validated in the Financial Management Tool project, ensuring the correct functionality and reliability of its features.


## 1. Introduction
- **Objective:**  
  Ensure that the test cases cover the entire project scope and verify that the tool operates efficiently, reliably, and without errors.
- **Scope:**
  - Validation of permission types  
  - Validation of the menus: Project List, Approvals, Reporting, and Gcraft  
  - Validation of the approval workflow  
  - Validation of project updates  
  - Validation of Capitalization and Negative CIP conditions  
  - Validation of report export functionality  
  - Validation of the app on different devices and in offline mode  

- **Referências:**
<details>
  <summary>📁 User Stories</summary>

 
Index | As | I Want to | So that
-- | -- | -- | --
1 | Product   Owner | Control CIP report | I can check what projects are open
2 | Product   Owner | Control CIP report | The Owner can be identified
3 | Product   Owner | have controls of user roles:   - Project Leader - users that only have access to update their project status   and information.   - Product Owner - have the ability to upload the GCRAFT master file, view all   project data and update any project data.   - Line Managers - Functional managers of the Project Leader with option to   view their team status of their group, can be multiple Line Managers for the   groups.   - Board approvers - board members with approval roles in the status update.   - Finance Manager - responsible / accountable for entire site control | system can have segregation of Duties (SoD)
4 | Product   Owner | have controls of groups, by creating a list where all users have   a group associated with (Engineering, finance, Quality, etc). | so details that line managers/stakeholders can view a   consolidaded list of projects from their team.
5 | Project   Leader | windows AD to be used for authentication | to assure compliance
6 | Project   Leader | windows AD to be used for approval flow | to assure approval history
7 | Product   Owner | I want to have an option to upload the GRAFT file inside the   APP. | the system can use this file to collect the data
8 | Project Leader | I want to have a welcome screen with option to Update   projects and Status of my projects | I can have visibility of historical data and update Quarter/Year   information
9 | Project   Leader | I want to have in a list form the projects under my name, pre-populated   with GCRAFT information, and the status (updaded or pending update). | I can easily know what project I need to update
10 | Project   Leader | I want to be able to select a project from my project list to   access project details and update information. | I can go into this project details tab to include the   information.
11 | Project   Leader | I want the details tab to have section, as below:   1. End Dates Reporting   2. Capitalization and Supplemental CAR   3. Negative CIP | I can go update each section
12 | Project   Leader | I want the details tab of End Dates Reporting with the   following fields:    1. Start Date and End Date (automatically from GCRAFT)   2. Latest Update in End Date (user input calendar option)   2.1 If user fills the New End Date, mandatory fields where I have input Rationale   and Upload file if needed   3. an Dropdown list with the following options on the picture to the   right | i can update the end dates section.
13 | Project   Leader | I want the details tab of Capitalization and Supplemental CAR   with the following fields:    1. field of "Start capitalization" to be drop down field:   1.1 Not applicable: only available as an option if end date is future date   1.2 Capitalization Started : only available as an option if end date has   passed current date.   1.3 Capitalization Started : only available as an option if end date has   passed current date.      2. the field of "higher than 80%" needs to calculated automatically   from the file and Yes/No needs to be flagged.   2.1 if Yes, the "suplemental CAR Required" needs to mandatory with   options Yes or No   2.2 If Yes for "suplemental CAR Required", the commentary fields is   required and the Attachment is optional.   If No, both needs to be blocked for input.      3. If user want to be move partial capitalization the tool must have a flag   of "Partial Capitalization" and    "Capitalization ID" and "Partial Amount" | i can update the capitalization Status.
14 | Project   Leader | I want the details tab of Negative CIP with the following   fields:    1. Field of "Negative CIP" to be automatically flagged with Yes or   No based on negative value on the GCRAFT File.   1.1 if Yes, the "Action for negative CIP" needs to mandatory with a   user inputed text field and an option with attachment is optional.   1.2 If No, the commentary fields and attachment field need to be blocked for   input.      I want to have a submit for approval button that will write all the   updates on the selected project. the project status needs to be changed to   Updated. | i can update the negative Status and update the overall status
15 | Project   Leader | if Capitalization started is select, I want the fielf of Capitalization ID to be mandatory   and allow for user input text.   If capitalization is not started, this Capitalization ID will be   blocked for inputs. | so I can indicate the GCRAFT Capitalization ID
16 | Product   Owner | I want to have a welcome screen with the User Story #8 plus the   feature to Upload the GCRAFT Quarter File | the system can use this file to collect the data
17 | Product   Owner | I want to receive an status of the upload of my file. If an   error, instruction of what to do next needs be provided. | I can easily identify if a error ocurred.
18 | Line   Managers | I want to have a welcome screen with the  options in US#8 plus the feature to view   reporting of my team (based on the groups defined list based on my Line   manager status). | so that I can a report view of the projects under by management
19 | Product Owner | the tool to automatically reads data from a GCRAFT Exported file   and maps the fields to create a quarter input | the tab report example colored in yellow can be automatically   filled.
20 | Line   Managers | An screen with project information needs to be available for   view only. Reports needs to have all project data and for user inputs ones a   history of the last 4 tool updates.   I want to have the ability to extract in excel or PDF a summary list of my   group reports. If PDF, include date of extraction and user that created   the extraction on the header. | reports can be created
21 | Product   Owner | An screen with project information needs to be available for   view only. Reports needs to have all project data and for user inputs ones a   history of the last 4 tool updates.   I want to have the ability to extract in excel or PDF a summary list of   all reports. If PDF, include date of extraction and user that created the   extraction on the header. | reports can be created
22 | Finance   Manager | An screen with project information needs to be available for   view only. Reports needs to have all project data and for user inputs ones a   history of the last 4 tool updates.   I want to have the ability to extract in excel or PDF a summary list of   all reports. If PDF, include date of extraction and user that created the   extraction on the header. | reports can be created
23 | Product   Owner | A flag must be automatically set for projects as follows:      1. if project information is the same status as the last update project status,   the project will be flagged as NO CHANGES.   2. If there are any changes on the project informtion, project status   flag needs to be INFORMATION CHANGES. | Approvers can easily identify project changes and speed up   approval.
24 | Product   Owner | After the governance review, I need to move all projects for   approval by the Board Approvers. | The approval workflow can begin.
25 | Board   Approvers | Have a "Pending Approval" screen in the app   that showcases all projects that need approval in a list.   The projects are organized with columns: Project Name and Flag   (Change/No Change).   The flag column must be able to filter projects (show only Changed/ show   only not changed / show all).      I need a main checkbox at the top to select all projects and individual   checkboxes for each project so that I can select/deselect individually.      I also need a button in the end for "Approve all selected"   or "Reject Selected".   For both of the buttons, a confirmation pop-up should appear, showing the   number of projects selected. e.g. "Are you sure you want to approve the   65 selected projects?" | ensure that the approval workflow is functional
26 | Board   Approvers | 1. For approved projects, no further action is needed.   Projects that are approved will be hidden from the "Pending   Approval" screen.      2. For rejected projects, move the user to a "Rejection Reason"   screen. There, all projects selected for rejection will require a text   comment input for the reason of rejection.   2.1. At the bottom of the page, I need a "Submit" button   which will only submit information when all text boxes are filled. | ensure that project rejections are justified.
27 | Product   Owner | Rejected projects must return as a "Draft" to the   "Update projects" screen for the Project Leader. | So that leaders can update information in a rejected project   based on the reject reason and send it for approval again.
28 | Board   Approvers | From the "Pending Approval" screen, I must also be able   to navigate to a list of "Approved" or navigate to a list of   "Rejected" projects. | I can view and manage projects that have already passed the   "Pending Approval" screen.
29 | Project   Leader | I want a receive an email notification once my project is with   status approved or submitted with no changes. Approvers and Line Manager   needs to receive this email as well. | can have better control of final project status
30 | Project   Leader | I want a receive an email notification once my project is   rejected with the rejection reason informed. | can have better control of final project status
31 | Line   Managers | I want a view in the reporting tag the last four end date for   each projects and a counter for total changes. | I can monitoring all projects    informations
32 | Product   Owner | I want a use the app to notify Project Leader 14 days prier the   governance meeting.   If the Project Leader Not update the tool automatically notify the direct   leader / line manager 7 day prier the governance meeeting   The product owner have to have a botton to block update status. | Project data is up to date and the Product Owner can use the   tool in the governance meeting

<!--EndFragment-->
</body>

</html>
</details>

## 2. Test Strategy

- **Test Types:**  
  - Functional tests
  - Regression tests
  - Integration tests
  - Performance tests
  - Exploratory tests

- **Test Levels:**  
  - System testing
  - Acceptance testing

- **Tools:**  
  - iOS and Android mobile phones
  - Tablets
  - MacBook

- **Test Environment:**  
  - Environment running the latest deployed version
  - Internet access
  - Mobile devices
  - Tablets
  - MacBook


## 3. Acceptance Criteria
- **Acceptance Criteria:**  
  All test scenarios must be executed successfully.


## 4. Test Execution Plan

- **Schedule:**  
  Test execution from 22/05/2025 to 26/05/2025

- **Responsible:**  
  Test Analyst Caroline Sousa

## 5. Test Cases

### 01. Test Case: Validation of Profile and Group Assignment

**Requirement Traceability:** 3 and 4  
**Objective:** Assign permissions to the users listed in the application


| Step | Action | Expected Result |
|------|--------|------------------|
| 1 | Access the application with the "Product Owner" profile | App redirects the user to the welcome screen with the following features:<br>- Project List<br>- Approvals<br>- Reporting<br>- Gcraft Master File |
| 2 | Access the settings icon in the upper right corner | App should display the "Users" submenu |
| 3 | Click on the Users list | App should allow viewing and editing users |
| 4 | Select a user and edit | App should display the following fields:<br>- Name<br>- Project<br>- Role<br>- Group |
| 5 | Click on Role | App should display the following profiles:<br>- Product Owner<br>- Project Leader<br>- Line Managers<br>- Board Approvers<br>- Financial Manager |
| 6 | Click on Group | App should display the following groups:<br>- Engineering<br>- Finance<br>- Quality |
| 7 | Assign one role and one group, then save | App should save the changes |
| 8 | Select the previous user > edit > remove the assigned role and save | App should **not** save the changes, since the role field is mandatory |
| 9 | Input a role and click save | The app should save the changes |
| 10 | Select the previous user > edit > remove the assigned group and save | App should **not** save the changes, since the group field is mandatory |
| 11 | Input a group and click save | App should save the changes |

### 02. Test Case: Login and Approval Validation using Windows AD

**Requirement Traceability:** 5 and 6  
**Objective:** Validate if the app accepts access via Windows AD


| Step | Action | Expected Result |
|------|--------|------------------|
| 1 | Access the App login screen | Login screen is displayed with "User" and "Password" fields |
| 2 | Enter valid Windows credentials and click "Login" | App should redirect the user to the home screen |
| 3 | Access the App login screen | Login screen is displayed with "User" and "Password" fields |
| 4 | Enter invalid Windows credentials and click "Login" | App should **not** redirect the user to the home screen and should display an "Invalid credentials" message |
| 5 | Enter valid Windows credentials for a "Board Approver" profile and click "Login" | App should redirect the user to the home screen |
| 6 | Click on the "Approvals" menu | App should display pending notifications for the project linked to the user's profile |
| 7 | Select a notification and click "Approve" | App should prompt the user to input Windows AD credentials |
| 8 | Enter incorrect user credentials and save | App should **not** approve the notification and should display an informational message |
| 9 | Select a notification and click "Approve" | App should prompt the user to input Windows AD credentials |
| 10 | Enter correct user credentials and save | App should approve the notification and send an email notification to the Project Leader |
| 11 | Access the notification history | App should display the approved notification in the history |
| 12 | Select a notification and click "Reject" | App should prompt the user to input Windows AD credentials |
| 13 | Enter incorrect user credentials and save | App should **not** reject the notification and should display an informational message |
| 14 | Select a notification and click "Reject" | App should prompt the user to input Windows AD credentials |
| 15 | Enter correct user credentials and save | App should reject the notification, require a reason, and return the feedback to the project list |
| 16 | Access the app with the "Project Leader" profile, make a change and send it for approval | App should send a notification to the Board Approvers |
| 17 | Access the "Approvals" menu and attempt to approve the change made by the same user | App should **not** allow it due to SoD (Segregation of Duties) restrictions |



### 03. Test Case: Validation of Open Projects View

**Requirement Traceability:** 1 and 2  
**Objective:** The app should list only open projects and identify their owners


| Step | Action | Expected Result |
|------|--------|------------------|
| 1 | Access the app with the "Product Owner" profile | App redirects the user to the welcome screen with the following features:<br>- Project List<br>- Approvals<br>- Reporting<br>- Gcraft Master File |
| 2 | Access the project list | App should display all projects registered in the application |
| 3 | Go to Filters section > Project Status > select "Open" option | App should list all projects that are currently open |
| 4 | Click on a project | App should display the person responsible for the project |


### 04. Test Case: Validation of GCRAFT File Upload

**Requirement Traceability:** 7, 16 and 17  
**Objective:** Allow the upload of the specific Gcraft file without error


| Step | Action | Expected Result |
|------|--------|------------------|
| 1 | Access the app with the "Product Owner" profile | App redirects the user to the home screen with the following features:<br>- Project List<br>- Approvals<br>- Reporting<br>- Gcraft Master File |
| 2 | Click on the "Gcraft Master File" menu | App should display the file upload field |
| 3 | Add a file of type Word, Excel, etc. | App should **not** allow the upload and should inform that only Gcraft files are accepted |
| 4 | Add multiple Gcraft Master File type files at once | App should **not** allow the upload and should inform that only a single file is accepted |
| 5 | Add a Gcraft file and simulate failure by disconnecting the internet | App should **not** complete the upload and should show an error message instructing the user to try again |
| 6 | Add a single Gcraft file and submit | App should complete the upload and display a success message |
|   | Access the app with a profile other than "Product Owner" | App should **not** enable the "Gcraft Master File" menu |


### 05. Test Case: Validation of Imported Fields in the Application

**Requirement Traceability:** 19  
**Objective:** Validate the automatic reading and input of data via file upload


| Step | Action | Expected Result |
|------|--------|------------------|
| 1 | Access the app with the "Product Owner" profile | App redirects the user to the welcome screen with the following features:<br>- Project List<br>- Approvals<br>- Reporting<br>- Gcraft Master File |
| 2 | Click on the "Gcraft Master File" menu | App should display the file upload field |
| 3 | Upload a Gcraft file that modifies project information | App should allow the upload, complete the input, and return a "successfully submitted" message |
| 4 | Upload another Gcraft file for the same project and submit | App should **not** allow it, as data must be submitted quarterly |
| 5 | Access the "Reporting" menu | App should display the updated project with the data inputted from the Gcraft file in step 3 |
| 6 | Access the app > "Reporting" menu using other profiles that have access to the updated project | App should display the data inputted via the Gcraft file |


### 06. Test Case: Validation of Report Creation and Export

**Requirement Traceability:** 20, 21 and 22 

**Objective:** Validate report export functionality in PDF and Excel formats


| Step | Action | Expected Result |
|------|--------|------------------|
| 1 | Access the app with the "Product Owner" profile | App should redirect the user to the home screen |
| 2 | Click on the "Reporting" menu | App should list projects with their data and update history |
| 3 | Try to edit the information in the report fields | App should **not** allow editing |
| 4 | Click the export button and select PDF | App should export the current screen content to PDF, including author name and date |
| 5 | Click the export button and select Excel | App should export the current screen content to Excel, including author name and date |
| 6 | Repeat the test using the "Line Manager" profile | App should behave the same as in previous steps |
| 7 | Repeat the test using the "Financial Manager" profile | App should behave the same, showing the report with a focus on financial fields |


### 07. Test Case: Validation of Project Changes

**Requirement Traceability:** 23  
**Objective:** The flag must automatically update the project status


| Step | Action | Expected Result |
|------|--------|------------------|
| 1 | Access the app with the "Product Owner" profile | App should redirect the user to the home screen |
| 2 | Upload a Gcraft file to modify project information | App should update the project data |
| 3 | Access the "Project List" menu and check the "Changes" column | App should automatically display a flag on the modified project indicating changes were made |
| 4 | Access the project and view its data | App should display the fields that were modified to the user |
| 5 | Complete the approval routine so the flag becomes inactive | App should display the project with the status "No Changes" |
| 6 | Upload a Gcraft file with the same already approved changes and access the "Project List" menu | App should continue showing the project with the status "No Changes" 


### 08. Test Case: Approval Workflow Validation

**Requirement Traceability:** 24, 25, 26 and 28  
**Objective:** Send approval notifications to the "Board Approvers"


| Step | Action | Expected Result |
|------|--------|------------------|
| 1 | Log in to the app with the "Product Owner" profile | App should redirect the user to the home screen |
| 2 | Access the "Project List" menu | App should display the projects linked to the user |
| 3 | Make changes to a project and send for approval | App should trigger approval notifications to the "Board Approvers" profile |
| 4 | Log in to the app with the "Board Approvers" profile | App should redirect the user to the home screen |
| 5 | Access the "Approvals" menu | App should display a "Pending Notifications" section |
| 6 | Select the "Pending Notifications" section and click on a notification | App should display the section with the following features:<br>- Project list<br>- Change column with Yes or No flags<br>- Filters<br>- Mass selection<br>- Approve and Reject buttons |
| 7 | Click on a notification and select the "Approve" button | App should show a confirmation popup: "Yes" or "No" |
| 8 | Click "No" | App should continue displaying the pending notification |
| 9 | Click on "Mass Selection" | App should select all pending notifications |
| 10 | Deselect mass selection | App should uncheck all pending notifications |
| 11 | Select a pending notification and click "Approve", then confirm | App should remove the notification from the pending list |
| 12 | Select a pending notification and click "Reject" | App should show a confirmation popup: "Yes" or "No" |
| 13 | Confirm the rejection | App should show a field to input a justification |
| 14 | Leave the justification field blank and click "Submit" | App should **not** allow submission, as the "Justification" field is mandatory |
| 15 | Fill in the justification | App enables the "Submit" button |
| 16 | Click the "Submit" button | App sends a draft to the "Project List" menu > Update Projects |
| 17 | Access the menu Approvals > Project List | App should display the list of Rejected and Approved projects |
| 18 | Navigate through the tabs | App should show the history of approved and rejected projects |



### 09. Test Case: Validation of Project Update and Notification Receipt

**Requirement Traceability:** 27, 29 and 30  
**Objective:** Profiles must receive email notifications related to the approval workflow



| Step | Action | Expected Result |
|------|--------|------------------|
| 1 | Log in to the app with the "Board Approvers" profile and reject a notification | App should send a notification to the "Project Leader" profile |
| 2 | The Project Leader should receive an email in their inbox | App should send a rejection email including comments and attachments |
| 3 | Log in to the app with the "Board Approvers" profile and approve a notification | App should send notifications to the Project Leader, Approvers, and Project Managers |
| 4 | Project Leader, Approvers, and Managers should receive an email in their inbox | App should send an approval email |
| 5 | Log in to the app with the "Project Leader" profile > go to Project List > Update Projects | App should display the projects that were rejected |
| 6 | Select the project and make corrections | App should display the "Submit for Approval" button |
| 7 | Click the "Submit for Approval" button | App should send an approval notification to the Board Approvers |

### 10. Test Case: Validation of Project Leader Profile View

**Requirement Traceability:** 8, 9, 10 and 11  
**Objective:** Verify that menus are displayed correctly for the "Project Leader" profile


| Step | Action | Expected Result |
|------|--------|------------------|
| 1 | Log in to the app with the "Project Leader" profile | App should display the home screen with "Project List" and "Approvals" |
| 2 | Click on the "Project List" | App should display only the projects linked to the user and their statuses |
| 3 | Analyze the project list | App should display the projects with the following characteristics:<br>- Projects in list format<br>- Fields populated with data from Gcraft<br>- "Status" column showing either "Updated" or "Pending" |
| 4 | Select a project | App should display the selected project with the following features:<br>- Project data<br>- Project history tab<br>- Update button<br>- Details filter |
| 5 | Click on the "Details" filter | App should show the following sections:<br>- Final Date Report<br>- Capitalization and Supplemental CAR<br>- Negative CIP |
| 6 | Click on "Update Project" | App should display data fields for Quarter/Year |


### 11. Test Case: Capitalization Functionality Validation

**Requirement Traceability:** 12, 13 and 15  
**Objective:** Verify that the validations for capitalization have been correctly implemented



| Step | Action | Expected Result |
|------|--------|------------------|
| 1 | Log in with the "Project Leader" profile > Go to Project List | App should display the projects linked to the user |
| 2 | Select a project where the end date is in the future > Details > Capitalization and Supplemental CAR | App should display the "Start Capitalization" field with the following option in the dropdown:<br>- Not Applicable |
| 3 | Select a project where the end date is in the past > Details > Capitalization and Supplemental CAR | App should display the "Start Capitalization" field with the following options in the dropdown:<br>- Capitalization not started<br>- Capitalization started |
| 4 | Select a project where the end date is in the past > Start Capitalization > value below 80% | App should display the field "Supplemental CAR required" with the option:<br>- No |
| 5 | Try to change the value to "Yes" | App should **not** allow the user to proceed |
| 6 | Select a project where the end date is in the past > Start Capitalization > value above 80% | App should display the "Supplemental CAR required" field with the options:<br>- Yes<br>- No |
| 7 | Select "Yes" | App should enable the comment and attachment fields |
| 8 | Try to proceed without filling in the fields | App should **not** allow progression because the fields are mandatory |
| 9 | Fill in the fields and proceed | App should display the "Partial Capitalization" field with options Yes or No |
| 10 | Select "No" | App should **not** proceed with partial capitalization |
| 11 | Select "Yes" | App should enable the fields for Capitalization ID and Partial Value |
| 12 | Try to proceed without filling in Capitalization ID and Partial Value | App should **not** allow it |
| 13 | Fill in Capitalization ID and Partial Value | App should allow progression |

### 12. Test Case: Negative CIP Functionality Validation

**Requirement Traceability:** 14  
**Objective:** Verify that validations for Negative CIP have been correctly implemented


| Step | Action | Expected Result |
|------|--------|------------------|
| 1 | Log in with the "Project Leader" profile > Project List | App should display the projects linked to the user |
| 2 | Select a project where the Gcraft file was updated with a negative value > Details > Negative CIP | The "Negative CIP" field should be automatically filled with the option "No" and the following fields should be locked:<br>- Comments<br>- Attachments |
| 3 | Select a project where the Gcraft file was updated with a positive value > Details > Negative CIP | The "Negative CIP" field should be automatically filled with the option "Yes" and the following fields should be enabled:<br>- Comments<br>- Attachments |
| 4 | Try clicking the "Submit for Approval" button | App should **not** enable the "Submit for Approval" button without filling in the "Comments" and "Attachments" fields |
| 5 | Fill in the "Comments" and "Attachments" fields | App should enable the "Submit for Approval" button |
| 6 | Log out of the app | App should continue showing the project with "Pending" status |
| 7 | Select a project where the Gcraft file was updated with a positive value > Details > Negative CIP | The "Negative CIP" field should be automatically filled with "Yes" and the following fields should be enabled:<br>- Comments<br>- Attachments |
| 8 | Fill in the "Comments" and "Attachments" fields and click "Submit for Approval" | App should update the project status to "Updated" and send an approval notification to the "Board Approvers" profile |

### 13. Test Case: Line Manager Profile Functionality Validation

**Requirement Traceability:** 18 and 31  
**Objective:** Verify that validations for the "Line Manager" profile have been correctly implemented


| Step | Action | Expected Result |
|------|--------|------------------|
| 1 | Log in to the app with the "Line Manager" profile | App should display the welcome screen with the "Project List" and "Reports" menus linked to the user's profile |
| 2 | Click on the "Reports" menu | App should show reports for the team under the manager's responsibility |
| 3 | Analyze the "Reports" menu | App should display, for each project, the last four final dates and a change counter |
| 4 | Log in with another profile and submit more than 4 final date modifications | App should update the history and change counter for the Line Manager |
| 5 | Log in to the app with the "Line Manager" profile > Reports > Project | App should update the last four final dates of the project and the change counter |



### 14. Test Case: Validation of Notification Sending to Project Leader

**Requirement Traceability:** 32  
**Objective:** Verify that notifications are being sent correctly


| Step | Action | Expected Result |
|------|--------|------------------|
| 1 | Log in to the app with the "Product Owner" profile | App should redirect the user to the home screen |
| 2 | Access the project list screen and change the date to 14 days before the governance meeting | App should send a notification to the Project Leader |
| 3 | Log in to the app with the "Project Leader" profile | App should display the notification generated in the previous step |
| 4 | Log in to the app with the "Product Owner" profile | App should redirect the user to the home screen |
| 5 | Access the "Project List" menu and change the date to 7 days before the governance meeting | App should send a notification to the Line Manager |
| 6 | Log in to the app with the "Line Manager" profile | App should display the notification generated in the previous step |
| 7 | Log in to the app with the "Product Owner" profile | App should redirect the user to the home screen |
| 8 | Access the project list screen and click the "Lock Updates" button | App should not allow project modifications |
| 9 | Log in with the "Project Leader" and "Line Manager" profiles | App should not allow project modifications |
| 10 | Log in with the "Product Owner" profile and unlock updates | App should allow project modifications |
| 11 | Log in with the "Project Leader" and "Line Manager" profiles | App should allow project modifications |


### 15. Test Case: Validation of Behavior Across Different Device Types

**Requirement Traceability:** Not applicable  
**Objective:** Verify how the application behaves on different devices


| Step | Action | Expected Result |
|------|--------|------------------|
| 1 | Repeat all previous test cases using iOS, Android, Tablet, and MacBook | App should be fully functional and responsive across all devices |


### 16. Test Case: App Offline Behavior Validation

**Requirement Traceability:** Not applicable  
**Objective:** Verify how the application behaves without internet connection


| Step | Action | Expected Result |
|------|--------|------------------|
| 1 | Log in to the app without an internet connection | App should allow offline viewing and navigation in all menus |
| 2 | Access the "Gcraft Master Files" menu and attempt to upload a file | App should inform the user that the upload can only be completed with an internet connection |
| 3 | Access the "Project List" menu, make unsaved changes, and close the app | App should **not** save the changes and should display the project with the previous status |
| 4 | Access the "Project List" menu and press the back arrow multiple times | App should display a pop-up asking if the user really wants to exit the application |

### 17. Test Case: Validation of Login on Multiple Devices

**Requirement Traceability:** Not applicable  
**Objective:** Verify how the application behaves when logging in with the same user on different devices  

| Step | Action | Expected Result |
|------|--------|------------------|
| 1 | Log in to the application using one profile | The app should log in using Windows AD |
| 2 | Log in to the application on a second device using the same user | The app should log in using Windows AD and prompt for approval to connect on the new device |


### 6. Risks and Mitigations
- Perform regression and exploratory testing to mitigate errors in product delivery.

### 7. Reports and Defect Logging
- Log bugs and improvements found in Azure DevOps.

### 8. Approvals
- The test plan must be approved by the AS2 Group team.


---




