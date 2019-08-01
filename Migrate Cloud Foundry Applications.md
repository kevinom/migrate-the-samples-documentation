# Migrate Cloud Foundry Applications on IBM Cloud
Date: 31 July 2019

This document provides an overview of the steps needed to migrate the Cloud Foundry sample applications from one IBM Cloud account to a different IBM Cloud account.
  
The IBM Cloud account where the samples are to be migrated and run must be owned by an IBM employee and the account must be upgraded to a *Pay As You Go* type of account.   
   
The steps provided in this document are only an overview of what should done. The person doing the migration should work with IBM Cloud Support by using the Live Chat at: <https://cloud.ibm.com/unifiedsupport/supportcenter> to ensure that all the steps are completed correctly.
## Current status
The Cloud Foundry applications are currently owned by the account that belongs to Kevin O'Mahony (**kevinom@ca.ibm.com**).   
This account will be invalidated when Kevin retires on September 6, 2019. The migration must be done prior to that date.    
The request for support from IBM Cloud has been requested in problem ticket CS0319597.   
Someone with an IBM Cloud account can review the ticket at <https://cloud.ibm.com/unifiedsupport/cases/manage/CS0319597?accountId=4e044ff6259729357f401515e48643f2>  
## Add the target user account to the Cloud account
In this step, you add the target user, assumed to be Tom Reed's IBM Cloud account to Kevin O'Mahony's IBM Cloud account.   

Sign on to IBM Cloud at <https://cloud.ibm.com/login>  
You are prompted to enter your IBM Id.  
Use the **kevinom@ca.ibm.com** account to sign on.   
The password for this Intranet Id will be supplied to Tom Reed in a separate corporate email.   

From the IBM Cloud account main menu, select **Manage > Access (IAM)**.   
Then, select **Users** from the navigation sidebar.    
Click **Invite Users**.   
 
Type the name of the target user in the **Email address** area.  
<img src="images/Screen Shot 2019-07-31 at 4.05.46 PM.png">   
     
Scroll down in the page to add the access for the target account.   
In the Services area of the page, the default value is to assign access to **Resource**.   
Scroll down in the page to add the Cloud Foundry access for the target account.   

Expand **Cloud Foundry access**  
Ensure that you select the details for Cloud Foundry applications:   
    
```
Organization=kevinom_org   

Organization roles=Manager   

Region=Dallas   

Space=All current spaces   

Space roles=Developer   
 
```   
   
<img src="images/Screen Shot 2019-07-31 at 4.17.56 PM.png">   
Scroll down in the page to add the user profile for the target account. 

Select **Super user** for the user profile.   
<img src="images/Screen Shot 2019-07-31 at 4.33.51 PM.png">    
Finally, click **Invite users** at the bottom of the page in IBM Cloud.    
The user is added as a super user to the list of users in the **kevinom@ca.ibm.com** account.

## Migrate the applications to the target user
According to the information in the IBM Cloud Support ticket <https://cloud.ibm.com/unifiedsupport/cases/manage/CS0319597> some action must still be taken for the target user to become the owner of the Cloud Foundry applications.   
Work with IBM Support to ensure that the target user account becomes the owner of the Cloud Foundry applications. This needs to be done before the **kevinom@ca.ibm.com** account is deleted, even if the target user is a super user on the account.   

## Review the applications in the target user
In this part, you verify that all the Cloud Foundry applications are indeed owned by the target IBM Cloud account.   
Sign on to IBM Cloud at <https://cloud.ibm.com/login>  
You are prompted to enter your IBM Id.  
Use the target account **treed1@us.ibm.com** account to sign on.  

From the default Dashboard you should see that 10 Cloud Foundry accounts are displayed.
<img src="images/Screen Shot 2019-07-31 at 4.50.29 PM.png">    
 
Expand the Cloud Foundry Apps to display the list of application samples.   
<img src="images/Screen Shot 2019-07-31 at 4.55.13 PM.png">      
The status of all of the applications should be **Running**.   

Congratulations!   
You have successfully migrated the Cloud Foundry applications from one IBM Cloud account to another IBM Cloud account.    
****   
