---
title: "Connect DefectDojo to Jira"
description: "Set up a Jira Configuration in DefectDojo - step 1 of working with Jira"
---

Jira Configurations are the starting point for DefectDojo’s Jira integration. You can add multiple configurations to a DefectDojo instance, to allow for many different linked Jira Projects and boards.




Adding a configuration does not cause any Findings to push right away \- this is simply the first step. Once the Jira Configuration is created, it must be added to a Product before any information will push to Jira. See **[this guide](https://support.defectdojo.com/en/articles/8490492-add-jira-integration-to-a-product)** for help with adding this integration to a Product.




# The Jira Configuration Page


The first step of setting up a Jira configuration is to add a Project to DefectDojo.



1. If you have not already done so, navigate to the System Settings page and check the box on **Enable Jira Integration**. You will need to do this before the ⚙️ **Configuration \> JIRA** option shows up on the sidebar.  
​
2. Navigate to the ⚙️**Configuration \> JIRA**  page from the DefectDojo sidebar.  
​


![](https://defectdojo-inc.intercom-attachments-7.com/i/o/923276103/2e774b44ee315e9f1fe41b82/CS6sI6mueuFgwwSbGtaqfxEbPRnlIzgfznaIsJIJWgbxgqvD2FPOy6PXxiuoYKrXCvw4iRCvOJyjEudrQHuseFZoBmFAAYp0Dg-NB-nVYdXA39tPOj2fEauP4SucvbaIYR7HQlb0s6-3Hew-pVpA5vY?expires=1729720800&signature=365f08fd7d42e19ebe17ab88fb023b7300567cbaea867f08b4153367e90597ac&req=fSIkFM54nIFcFb4f3HP0gCxFHutEmNqH7jYG931BvciUfy74oWsSnQSSvalx%0A5%2Fo%3D%0A)
  
​
3. You will see a list of all currently configured JIRA Projects which are linked to DefectDojo. To add a new Project Configuration, click the wrench icon and choose either the **Add JIRA Configuration (Express)** or **Add JIRA Configuration** options.


# Add JIRA Configuration (Express)


The Express method allows for a quicker method of linking a Project. Use the Express method if you simply want to connect a Jira Project quickly, and you aren’t dealing with a complex Jira workflow.




![](https://defectdojo-inc.intercom-attachments-7.com/i/o/923276110/e56e505a6376018b2122b7fe/Ctw3ngxgjcN7GtRhu3UQvuXL6kRB7KXN8hrXgvmKIDsU48fDs2_YykUh_TsnbLzPwS0tmYWE92ESBPZyJUIThf4JcE0iMI3djceRKMoRAK54cuO9ywYZQTuS08D1KOzzb_SPO7t1_G6yigZ6X-EIMpM?expires=1729720800&signature=2e0fa3eb0ed45007c00921a283becb9861dda2d02d8ec30dc8ee3d70e704c9ee&req=fSIkFM54nIBfFb4f3HP0gKND0q%2BqhfaNsoM%2F9w6HI86zepJ7GdfOwgfRYqPB%0A34s%3D%0A)

1. Select a name for this Jira Configuration to use on DefectDojo.  
​
2. Select the URL for your company’s Jira instance \- likely similar to https://**yourcompany**.atlassian.net if you’re using a Jira Cloud installation.  
​
3. Enter your Username and Password for Jira. Alternatively, if your Jira instance uses a Personal Access Token (**PAT**) for authentication, you should instead enter the **PAT** in the Password field. The Username will not be used for authentication with **PAT**, but you can use this field as a label to indicate the name of the **PAT** you're using.  
​
4. Select the Default issue type which you want to create Issues as in Jira. The options for this are **Bug, Task, Story** and **Epic** (which are standard Jira issue types) as well as **Spike** and **Security**, which are custom issue types. If you have a different Issue Type which you want to use, please contact [support@defectdojo.com](mailto:support@defectdojo.com) for assistance.  
​
5. Select your Issue Template \- the two types are:  
\- **Jira\_full**, which will include all Finding information in Jira Issues  
\- **Jira\_limited**, which will include a smaller amount of Finding information and metadata.  
​  
If you leave this field blank, it will default to **Jira\_full.**  
​
6. Select one or more Jira Resolution types which will change the status of a Finding to Accepted (when the Resolution is triggered on the Issue). If you don’t wish to use this automation, you can leave the field blank.  
​
7. Select one or more Jira Resolution types which will change the status of a Finding to False Positive (when the Resolution is triggered on the Issue). If you don’t wish to use this automation, you can leave the field blank.  
​
8. Decide whether you wish to send SLA Notifications as a comment on a Jira issue.  
​
9. Decide whether you wish to automatically sync Findings with Jira. If this is enabled, Jira Issues will automatically be kept in sync with the related Findings. If this is not enabled, you will need to manually push any changes made to a Finding after the Issue has been created in Jira.  
​
10. Select your Issue key. In Jira, this is the string associated with an Issue (e.g. the word **‘EXAMPLE’** in an issue called **EXAMPLE\-123**). If you don’t know your issue key, create a new Issue in the Jira Project. In the screenshot below, we can see that the issue key on our Jira Project is **DEF**.  
​


![](https://defectdojo-inc.intercom-attachments-7.com/i/o/923276116/18a309f58113bed538edef5c/qtggrY2_20z4Jp6uz7dxaohMrHzmJn9DXelFKtR2wGnD8ByE8ROC1SiWcEtuR1qKqkDPhXGbzHHKd6NnQ-uHpQKUTfEQ253GTmbxAEWYiKRue7SVKdzJTj3BB2EBKrRg1ersE6Yi_Xzxbh9W98LFC4w?expires=1729720800&signature=f918416686d1ccbe7ba658303ad0567c5bd97d202e5583e0fd49549664c2e73e&req=fSIkFM54nIBZFb4f3HP0gIg8xes%2B%2Baq6uUPJoKLs5nKEcgU4E2h07lSJKI99%0Apd0%3D%0A)
​
11. Click **Submit.** DefectDojo will automatically look for appropriate mappings in Jira and add them to the configuration. You are now ready to link this configuration to one or more Products in DefectDojo.


# Add Jira Configuration (Standard)


The Standard Jira Configuration adds a few additional steps to allow for more precise control over Jira mappings and interactions. This can be changed after a Jira configuration has been added, even if it was created using the Express method.  
​


## Additional Configuration Options


* **Epic Name ID:** If you have multiple Epic types in Jira, you can specify the one you want to use by finding its ID in the Jira Field Spec.  
​  
To obtain the 'Epic name id' visit https://\<YOUR JIRA URL\>/rest/api/2/field and search for Epic Name. Copy the number out of cf\[number] and paste it here.  
​  
​
* **Reopen Transition ID:** If you want a specific Jira Transition to Reopen an issue, you can specify the Transition ID here. If using the Express Jira Configuration, DefectDojo will automatically find an appropriate Transition and create the mapping.  
​  
Visit https://\<YOUR JIRA URL\>/rest/api/latest/issue/\<ANY VALID ISSUE KEY\>/transitions? expand\-transitions.fields to find the ID for your Jira instance. Paste it in the Reopen Transition ID field.  
​  
​
* **Close Transition ID:** If you want a specific Jira Transition to Close an issue, you can specify the Transition ID here. If using the **Express Jira Configuration**, DefectDojo will automatically find an appropriate Transition and create the mapping.  
​  
Visit https://\<YOUR JIRA URL\>/rest/api/latest/issue/\<ANY VALID ISSUE KEY\>/transitions? expand\-transitions.fields to find the ID for your Jira instance. Paste it in the Close Transition ID field.  
​  
​
* **Mapping Severity Fields:** Each Jira Issue has an associated Priority, which DefectDojo will automatically assign based on the Severity of a Finding. Enter the names of each Priority which you want to map to, for Info, Low, Medium, High and Critical Severities.  
​  
​
* **Finding Text** \- if you want to add additional standardized text to each Issue created, you can enter that text here. This is not text that maps to any field in Jira, but additional text that is added to the Issue Description. "**Created by DefectDojo**" for example.


Comments (in Jira) and Notes (in DefectDojo) can be kept in sync. This setting can be enabled once the Jira configuration has been added to a Product, via the **Edit Product** form.






# Next steps


Now that you've set up your Jira Configuration, **[link it to one or more of your Products](https://support.defectdojo.com/en/articles/8490492-add-jira-integration-to-a-product)** to have your Findings populate into Jira.

