# Phase 2: Org Setup & Configuration - Deliverables

This document provides a step-by-step visual and descriptive walkthrough of the setup and configuration performed in Phase 2 for the Retail CRM project.

---

### 1. Company Information

**Description:** The organization was set up as "Retail CRM Pvt Ltd". The default time zone was configured to **(GMT+05:30) India Standard Time (Asia/Kolkata)** to ensure all date and time fields align with the project's regional context.

![Company Information](https://raw.githubusercontent.com/Sathwik231012/Retail-CRM-Salesforce-Project/main/Phase%202/Phase2_02_CompanyInformation.png)

---

### 2. Business Hours & Holidays

**Description:** Business hours were established for **Monday through Saturday, 9:00 AM to 9:00 PM IST**. Sunday is designated as a non-working day, preventing case escalations. Key national holidays were also added to manage service level agreements accurately.

![Business Hours](https://raw.githubusercontent.com/Sathwik231012/Retail-CRM-Salesforce-Project/main/Phase%202/Phase2_03_BusinessHours.png)

![Holidays](httpse://raw.githubusercontent.com/Sathwik231012/Retail-CRM-Salesforce-Project/main/Phase%202/Phase2_03_Holidays.png)

---

### 3. User & Role Management

**Description:** Five users were created to simulate the core retail team. A role hierarchy was then established to model the organizational structure, ensuring a proper chain of command for data visibility and reporting.

**Note on Licenses:** Due to Developer Edition license limits, the Marketing Manager and Regional Manager were created with Chatter licenses and thus are not part of the formal role hierarchy, demonstrating an understanding of platform constraints.

![Users List](https://raw.githubusercontent.com/Sathwik231012/Retail-CRM-Salesforce-Project/main/Phase%202/Phase2_05_Users_List.png)

![Role Hierarchy](https://raw.githubusercontent.com/Sathwik231012/Retail-CRM-Salesforce-Project/main/Phase%202/Phase2_06_Roles.png)

---

### 4. Custom Profiles & Permission Sets

**Description:** To manage permissions granularly, the standard user profile was cloned to create a **Sales Agent Profile** and a **Service Agent Profile**. Additionally, an **"Export Reports" Permission Set** was created to grant specific users extra capabilities without altering their base profile.

![Profiles List](https://raw.githubusercontent.com/Sathwik231012/Retail-CRM-Salesforce-Project/main/Phase%202/Phase2_06_Profiles_List.png)

![Permission Sets](https://raw.githubusercontent.com/Sathwik231012/Retail-CRM-Salesforce-Project/main/Phase%202/Phase2_06_PermissionSets.png)

---

### 5. Sharing Model (OWD & Sharing Rules)

**Description:** The security model was established by setting the `Order` object's Organization-Wide Default (OWD) to **Private**. This ensures records are secure by default. An owner-based sharing rule was then created to grant the Marketing Group **Read-Only** access to orders owned by Sales Agents.

![OWD Settings](https://raw.githubusercontent.com/Sathwik231012/Retail-CRM-Salesforce-Project/main/Phase%202/Phase2_07_OWD.png)

![Sharing Rule for Orders](https://raw.githubusercontent.com/Sathwik231012/Retail-CRM-Salesforce-Project/main/Phase%202/Phase2_08_SharingRule_Orders.png)

---

### 6. Access Policies

**Description:** User access was secured through Login Hours and strengthened password policies. Login hours for the Sales Agent profile were restricted to business hours to prevent off-hour access. Org-wide password policies and session timeouts were configured to enhance overall security.

![Login Hours](https://raw.githubusercontent.com/Sathwik231012/Retail-CRM-Salesforce-Project/main/Phase%202/Phase2_09_LoginHours_SalesAgent.png)

![Password Policies](https://raw.githubusercontent.com/Sathwik231012/Retail-CRM-Salesforce-Project/main/Phase%202/Phase2_09_PasswordPolicies.png)

![Session Settings](https://raw.githubusercontent.com/Sathwik231012/Retail-CRM-Salesforce-Project/main/Phase%202/Phase2_09_SessionSettings.png)

---

### 7. Field-Level Security (FLS) & Page Layouts

**Description:** A custom `Service Level` field was created on the Order object. FLS was configured to make this field **editable for Sales Agents** but **Read-Only for Service Agents**. The field was then added to the appropriate page layout to be visible to users.

**<-- IMPORTANT: ADD YOUR FLS SCREENSHOT HERE -->**
![FLS for Service Level](https://raw.githubusercontent.com/Sathwik231012/Retail-CRM-Salesforce-Project/main/Phase%202/Phase2_07_FLS_ServiceLevel.png)

![Page Layout](https://raw.githubusercontent.com/Sathwik231012/Retail-CRM-Salesforce-Project/main/Phase%202/Phase2_07_PageLayout_SalesAgent.png)

---

### 8. Final Verification

**Description:** The security configurations were verified by logging in as both the Sales and Service Agents. The Sales Agent was able to create and edit the `Service Level` field. The Service Agent was able to see the field, but it was correctly locked and read-only, confirming that all security settings were working as designed.

![Sales Agent View (Editable)](https://raw.githubusercontent.com/Sathwik231012/Retail-CRM-Salesforce-Project/main/Phase%202/Phase2_08_SalesAgent_CreateOrder.png)

**<-- IMPORTANT: ADD YOUR SERVICE AGENT READ-ONLY SCREENSHOT HERE -->**
![Service Agent View (Read-Only)](https://raw.githubusercontent.com/Sathwik231012/Retail-CRM-Salesforce-Project/main/Phase%202/Phase2_08_ServiceAgent_ReadOnly.png)
