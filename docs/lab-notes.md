# 📄 Lab Notes: SC-200 Microsoft 365 Security Tenant

- **Author**: Andre Patterson
- **Environment**: Microsoft 365 E5 Trial | Microsoft Entra ID | Default Directory
- **Course**: Microsoft SC-200 – Security Operations Analyst (Udemy)

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Lab 1 - Microsoft 365 Tenant & Entra ID Setup

**Objective**: Stand up the tenant and establish the Entra ID identity foundation everything else builds on.

**Step 1 - Navigate to Entra ID**
From the Microsoft Azure homepage, selected the top left menu icon, then selected Entra.
![Navigate to Entra ID](../screenshots/lab1-tenant-entra-setup/01-image9.png)



**Step 2 - Open Users**
Selected **Users** from the Entra ID navigation.
![Navigate to Entra ID](../screenshots/lab1-tenant-entra-setup/02-image10.png) 



**Step 3 - Create New User**
Selected **+ New user** icon, 
![Navigate to Entra ID](../screenshots/lab1-tenant-entra-setup/03-image11.png)








Then **Create new user**.
![Navigate to Entra ID](../screenshots/lab1-tenant-entra-setup/04-image12.png)






**Step 4 - Assign Directory Role**
Selected **Assignments**, 
![Navigate to Entra ID](../screenshots/lab1-tenant-entra-setup/05-image13.png)







then **+ Add role**, which displayed the Directory roles panel.
![Navigate to Entra ID](../screenshots/lab1-tenant-entra-setup/06-image14.png)




**Step 5 - Select Global Administrator**
Searched "Global Admin" in the search field, selected the **Global Administrator** box (blue tick displayed), then clicked **Select**.
![Navigate to Entra ID](../screenshots/lab1-tenant-entra-setup/07-image15.png)




**Step 6 — Review and Create**
Selected **Review + create** to confirm the new admin account configuration.
![Navigate to Entra ID](../screenshots/lab1-tenant-entra-setup/08-image16.png)



then click **Create**.
![Navigate to Entra ID](../screenshots/lab1-tenant-entra-setup/09-image17.png)


Lab 1 complete ✅


--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Lab 2 - Microsoft 365 E5 Trial & Domain Configuration

**Objective**: Provision the E5 licence tier required for Defender XDR, Sentinel integrations and other security tooling.

**Step 1 - Start the E5 Trial**
Marketplace → Microsoft 365 E5 → Start free trial.
![Navigate to Entra ID](../screenshots/lab2-e5-trial-domain/01-image21.png)



**Step 2 - Verify Licence**
Selected Billing → Licences and confirmed Microsoft 365 E5 was displayed under Licences.
![Navigate to Entra ID](../screenshots/lab2-e5-trial-domain/03-image24.png)

Lab 2 complete ✅

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Lab 3 - Administrative Account Separation of Duties

**Objective**: Create two distinct administrative accounts - a Global Administrator and a dedicated Security Administrator, rather than a single all-powerful login.

**Step 1 - Create Lab Admin_1**
Users → Active users → Add a user. Under the tenant domain, added admin account **Lab Admin_1**
![Navigate to Entra ID](../screenshots/lab3-admin-accounts/01-image27.png)



**Step 2 - Assign E5 Licence**
Lab Admin_1 requires access to Microsoft security products such as MS XDR, MS Sentinel integrations, and MS Defender for Endpoint, so a **Microsoft 365 E5** licence was assigned by ticking the box to enable these capabilities.
![Navigate to Entra ID](../screenshots/lab3-admin-accounts/02-image28.png)



**Step 3 - Assign Global Administrator Role**
Selected **Admin center access** under Roles, then ticked **Global Administrator**. Clicked Next to progress to the Review and finish page.
![Navigate to Entra ID](../screenshots/lab3-admin-accounts/03-image29.png)



**Step 4 — Confirm and Close**
Reviewed the admin user data, selected **Finish adding**, confirmed **Lab Admin_1** was created
![Navigate to Entra ID](../screenshots/lab3-admin-accounts/04-image30.png)






Then selected **Close**. 
![Navigate to Entra ID](../screenshots/lab3-admin-accounts/05-image31.png)








Lab Admin_1 is now displayed as an Active user with a Microsoft 365 E5 licence assigned.
![Navigate to Entra ID](../screenshots/lab3-admin-accounts/06-image32.png)









**Step 5 - Create a Dedicated Security Operations Account**
Selected **Add a user** to create a second account, used for investigations and threat-hunting activities throughout this project. Filled in the basic information for this **Security Analyst** user account.
![Navigate to Entra ID](../screenshots/lab3-admin-accounts/07-image33.png)









**Step 6 - Assign Licence and Security Administrator Role**
Assigned the same E5 licence. 
![Navigate to Entra ID](../screenshots/lab3-admin-accounts/08-image34.png)







Under Roles, selected **Admin center access**, scrolled to the **Security & Compliance** section, and selected **Security Administrator**, providing access to Microsoft security products without granting full tenant-wide administrative permissions
![Navigate to Entra ID](../screenshots/lab3-admin-accounts/09-image35.png)







**Step 7 - Confirm**
Reviewed all information and selected **Finish adding**. 
![Navigate to Entra ID](../screenshots/lab3-admin-accounts/10-image36.png)









Both **Lab Admin_1** and the **Security Analyst** admin account are now Active users assigned Microsoft 365 E5 licences - these accounts are used for the remainder of the project.
![Navigate to Entra ID](../screenshots/lab3-admin-accounts/12-image38.png)

Lab 3 complete ✅


--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## Lab 4 - Standard User Provisioning (Least Privilege)

**Objective**: Provision standard employee accounts with no administrative access, to represent a realistic organisation for future sign-in activity, device enrolment, investigations and attack-simulation exercises.


**Step 1 - Create First Standard User**
Via Add a user, created **John Smith** 
![Navigate to Entra ID](../screenshots/lab4-standard-users/01-image39.png)

along with a password, and assigned a Microsoft 365 E5 licence, ensuring the user can participate in future Microsoft Defender, Intune, and identity-related labs.
![Navigate to Entra ID](../screenshots/lab4-standard-users/02-image40.png)



**Step 2 — Apply Least Privilege**
Following the principle of least privilege, standard users should only have the permissions required for their daily tasks. Ensured **User (no admin center access)** was selected, then clicked Next.
![Navigate to Entra ID](../screenshots/lab4-standard-users/03-image41.png)




**Step 3 — Review and Finish**
Reviewed the settings
![Navigate to Entra ID](../screenshots/lab4-standard-users/04-image42.png)


And selected **Finish adding**, then **Close**.
![Navigate to Entra ID](../screenshots/lab4-standard-users/05-image43.png)



**Step 4 — Create Additional Standard Users**
Created four further standard user accounts following the same pattern, visible on the Active users page.
![Navigate to Entra ID](../screenshots/lab4-standard-users/07-image45.png)


Lab 4 complete ✅

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


## Lab 5 - Microsoft Defender XDR: Incident Alert Notifications

**Objective**: Configure alert email notifications in Defender XDR so security teams are informed automatically when important security events are detected.


**Step 1 - Navigate to Defender XDR Settings**
Show navigation → System → Settings → Microsoft Defender XDR.
![Navigate to Entra ID](../screenshots/lab5-defender-xdr-alerts/01-image48.png)







**Step 2 - Open Email Notifications**
Within Microsoft Defender XDR, selected **Email notification**. Email notifications allow organisations to automatically notify security personnel whenever incidents matching specific criteria are generated, ensuring important security events are communicated to the appropriate teams for investigation and response.
![Navigate to Entra ID](../screenshots/lab5-defender-xdr-alerts/02-image49.png)






**Step 3 — Create a Notification Rule**
Selected **+ Add incident notification rule**
![Navigate to Entra ID](../screenshots/lab5-defender-xdr-alerts/03-image50.png)




I then provide a **name** and **description** for this notification email rule to make it easier for analyst to identify. 
![Navigate to Entra ID](../screenshots/lab5-defender-xdr-alerts/04-image51.png)


**Step 4 — Scope by Severity**
Under Alert severity, selected both **Medium** and **High** severity incidents,  a scoping choice commonly used by security teams to capture important incidents without generating excessive notification noise. Clicked Next.

![Navigate to Entra ID](../screenshots/lab5-defender-xdr-alerts/07-image54.png)




**Step 5 - Add Recipient**
Used the admin address as the recipient of the alerts, then clicked Add. Verified the admin address appeared in the list of recipients, meaning notifications would be received when incidents occur.

![Navigate to Entra ID](../screenshots/lab5-defender-xdr-alerts/08-image55.png)



**Step 6 - Review and Submit**
Reviewed the summary page (rule name, source selection, severity levels, recipient information) and clicked **Submit**. 
![Navigate to Entra ID](../screenshots/lab5-defender-xdr-alerts/10-image57.png)


The new notification rule was created successfully.
![Navigate to Entra ID](../screenshots/lab5-defender-xdr-alerts/11-image58.png)


--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


## Lab 6 - Microsoft Defender for Endpoint (In Progress)

Extending the tenant into Microsoft Defender for Endpoint as part of ongoing SC-200 coursework. Notes and screenshots to follow as this lab is completed.

