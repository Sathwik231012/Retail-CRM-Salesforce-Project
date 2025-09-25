# Phase 2: Org Setup & Configuration

## Summary

This phase involved setting up the foundational structure of the Salesforce environment for the Retail CRM project. The configuration includes company information, user and role setup, and a comprehensive security model to ensure data visibility and access are correctly managed. This setup provides the essential framework for building the application's features in the subsequent phases.

---

## Key Configurations

### Company & Org Setup
- **Company Information**: The organization was set up as "Retail CRM Pvt Ltd" with the default time zone set to **(GMT+05:30) India Standard Time (Asia/Kolkata)**.
- **Business Hours & Holidays**: Business hours were established for **Monday-Saturday, 9:00 AM to 9:00 PM IST**. Sunday is configured as a non-working day. Key national holidays were added to manage service level agreements accurately.
- **Fiscal Year**: A **Custom Fiscal Year** was enabled to run from April to March, aligning with standard Indian business and tax cycles.

### User & Role Management
- **Users Created**: Five users were created to simulate the retail team:
  - **Salesforce License Users**: System Admin, Sales Agent, Service Agent.
  - **Chatter License Users**: Marketing Manager, Regional Manager (*see license note below*).
- **Role Hierarchy**: A role hierarchy was established to model the organizational structure, with the CEO at the top, followed by managers and agents.

---

## Security Model

### Profiles & Permission Sets
- **Custom Profiles**: The standard `Standard User` profile was cloned to create a `Sales Agent Profile` and a `Service Agent Profile`, allowing for specific object and field permissions.
- **Permission Sets**: An **"Export Reports"** permission set was created to grant specific users the ability to export report data without altering their base profile.

### Sharing & Visibility
- **Organization-Wide Defaults (OWD)**: The `Order` object's default internal access was set to **Private** to ensure that users can only see records they own by default.
- **Sharing Rules**: An owner-based sharing rule was created to grant the Marketing Group **Read-Only** access to all orders owned by users in the Sales Agent role.
- **Field-Level Security (FLS)**: FLS was configured for the custom `Service Level` field on the Order object, making it editable for Sales Agents but **Read-Only** for Service Agents.

### Access Policies
- **Login Hours**: Login hours for the `Sales Agent Profile` were restricted to business hours **(Monday-Saturday, 9:00 AM - 9:00 PM IST)**, preventing off-hour access.
- **Password Policies**: Org-wide password policies were strengthened to require a 90-day expiration and complexity including letters and numbers.
- **Session Settings**: The session timeout was set to 2 hours of inactivity for enhanced security.

---

## Important Note on License Limitations

Due to the license limitations in a Salesforce Developer Edition org, the **Marketing Manager** and **Regional Manager** roles were created using Chatter Free/Moderator licenses. As these licenses do not support Role assignments or full CRM object access, they were excluded from the Role Hierarchy. This approach demonstrates an understanding of managing user setup within real-world platform constraints.

---

## Deliverables (Screenshots)

1.  `Phase2_02_CompanyInformation.png`
2.  `Phase2_03_BusinessHours.png`
3.  `Phase2_03_Holidays.png`
4.  `Phase2_05_Users_List.png`
5.  `Phase2_06_Roles.png`
6.  `Phase2_06_Profiles_List.png`
7.  `Phase2_06_PermissionSets.png`
8.  `Phase2_08_SharingRule_Orders.png`
9. `Phase2_09_LoginHours_SalesAgent.png`
10. `Phase2_07_FLS_ServiceLevel.png`
11. `Phase2_07_PageLayout_SalesAgent.png`
12. `Phase2_08_SalesAgent_CreateOrder.png`
13. `Phase2_08_ServiceAgent_ReadOnly.png`
14. `Phase2_09_SessionSettings.png`
15. `Phase2_09_PasswordPolicies.png`
