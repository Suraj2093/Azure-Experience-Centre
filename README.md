 
# Azure-Experience-Centre

<br><br>

<!-- TOC -->
1. [Getting Started](#getting-started)
 * [1.1: Logging to Management Portal](#1.1-logging-to-management-portal)
2. [Creating AEC Templates](#Creating-aec-templates)

 

    

<!-- /TOC -->

# Getting Started

## 1.1: Logging to Management Portal

### Home Page Overview

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/Portal_overview.png"/>  

### How to login to AEC
- Navigate to the portal using the link https://experience-azure-mgmt.azurewebsites.net/#/main.
- Click on the **Log In** button on the top right portion of the page.  

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/portal_login.png"/>

- On clicking **Log In** button, you will be redirected to the following page.
- Enter your Email address and click on Next.

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/portal_login1.png"/>

- Enter the password for your account and click on Sign in

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/Login_password.png"/>

### How to logout from AEC
-To logout from the portal, Click on the button with your username on the top right hand side of the page. A drop down list will be displayed. Click on logout and you will be logged out and will be redirected to the home page.

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/Logout.png"/>

## Creating AEC templates

### Create Template
-Navigate to the portal using the link https://experience-azure-mgmt.azurewebsites.net/#/main and login with your AEC credentials.  
-Once logged in, click on **Templates** on the left pane of the portal. This will list the templates if any.  

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/templates.png"/>

-Click on **ADD** at the top right corner of the templates page, to add a new template.  

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/add_template.png"/>

-Now provide the following details in the Add Template page that comes up.  
* Name : Provide a suitable name to the template.
* Code : Provide an identifyable course code.
* Description : Enter the description of the template.  
* ARM Template URL(optional) : Upload the ARM template that automate the required resources for the event, to storage and provide the template link.  
* Parameter Template URL(optional) : Upload the Parameter template that is used in the ARM template, to storage and provide the parameter template link.  
* Owner Email : Provide the email ID of the owner of the workshop.  
* Deployment Plan : Choose any of the deployment plan as below
<br> a. [Single Resource Group](#single-resource-group) : Choose this plan if you need only one resource group for the workshop to deploy.
<br> b. [Shared Instance](#shared-instance) : Choosing this plan will provide one resource group for all the attendees in the workshop.
<br> c. [Resource Group - Two](#resource-group-two) : Choose this plan if you need two resource group for the workshop to deploy.
<br> d. [Resource Group - Three](#resource-group-three) : Choose this plan if you need three resource group for the workshop to deploy.
<br> e. [Resource Group - Four](#resource-group-four) : Choose this plan if you need four resource group for the workshop to deploy.   
<br> f. [Resource Group - Five](#resource-group-five) : Choose this plan if you need five resource group for the workshop to deploy.

* Lab Guide URL(optional) : Upload the lab guide for the workshop, to storage and provide the lab guide link. 
* Demo URL(optional) : Provide the link to sample or quickstart.  
* PPT URL(optional) : Provide link to presentation slides.  
* Prerequisites URL(optional) : Provide the link to prerequisites URL(if any).  
* Regions : Provide the regions where you want to deploy the template.
* MS Cloud Licenses(optional) : Choose the license which you want to assign to the user for the lab.
* Create Service Principal(optional) : Check this option if you want to create separate service principle for each of the users registered for the lab.
* Send Service Principal(option comes up only if you check the above option) : Check this option if you want to send the service principle details to each of the users registered for the lab. The details will be sent with the lab details.
* Attendee Custom RBAC URL(optional) : Create custom RBAC policies for the attendees in the workshop and upload in storage. Provide the link to policy here. 

-Click on **Submit** once required options above are filled.

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/add_template_details.png"/>

-Click on **Edit Icon** to edit the created template and add the template permissions if any

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/Template_Edit.png"/>

* Permission Type : Choose any of the Permission type as below
<br> a. [Azure Built-in Role](#azure-built-in-role) : Choose this permission type to assign the Azure Built-in Role to the Attendee/Instructor of the workshop.
<br>* [Profile Type](#profile-type) : Choose Attendee or Instructor according to whom you want to assign this permission.
<br>* [Identity](#identity) : Choose AAD user or AAD Service Principle according to where you want to apply this permission.
<br>* [Scope Type](#scope-type) : Choose Azure to set this permission scope level at Azure
<br>* [Scope Level](#scope-level) : Choose scope level as RG level or subscription level to set the scope level of this permission.
<br>* [Permission](#permission) : Choose the permission as Reader or Owner or contributor from the drop down according to what permission you want to assign to the Attendee/Instructor.
<br>* [Apply at Launch](#apply-at-launch) : Check this option if you want to apply the permission at the time of deployment of the template

-Click on **Submit** once required options above are filled.
 
<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/Azure_built-in_role.png"/>

<br> b. [Custom ARM Policy](#custom-arm-policy) : Choose this permission type to assign the Custom ARM Policy to whoever is using the Resource group or Subscription of the workshop.
<br>* [Scope Type](#scope-type) : Choose Azure to set this permission scope level at Azure
<br>* [Scope Level](#scope-level) : Choose scope level as RG level or subscription level to set the scope level of this policy you are going to upload.
<br>* [Permission Data](#permission-data) : Enter the Custom policy URL of where you have uploaded the Policy file. These policies will be applied to the users using the workshop according to the Scope Level.
<br>* [Apply at Launch](#apply-at-launch) : Check this option if you want to apply the policy at the time of deployment of the template

-Click on **Submit** once required options above are filled.
 
<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/Custom_policy.png"/>

<br> a. [Azure Custom Role](#azure-custom-role) : Choose this permission type to assign the Azure Custom Role to the Attendee/Instructor of the workshop.
<br>* [Profile Type](#profile-type) : Choose Attendee or Instructor according to whom you want to assign this role.
<br>* [Identity](#identity) : Choose AAD user or AAD Service Principle according to where you want to apply this custom role.
<br>* [Scope Type](#scope-type) : Choose Azure to set this custom role scope level at Azure
<br>* [Scope Level](#scope-level) : Choose scope level as RG level or subscription level to set the scope level of this custom role.
<br>* [Permission Data](#permission-data) : Enter the Custom permission URL of where you have uploaded the RBAC file. These roles will be applied to the Attendee/Instructor according to the Scope Level.
<br>* [Apply at Launch](#apply-at-launch) : Check this option if you want to apply the custom role at the time of deployment of the template

-Click on **Submit** once required options above are filled.
 
<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/custom_role.png"/>

-Once all the permissions are added to the template, please click on **Submit** above the template Permissions section.  

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/permissions_template.png"/>

-Click on **Validate subscription with ARM template** icon corresponding to the template created.  

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/Template_validate.png"/>

-Provide the azure subscription group and subscription in which the validator should be run. Also provide the regions where you want to validate the template and click on **Submit**.  

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/validation_details.png"/>

### Use of template outputs
-If you want to provide the attendees some results that are required in the workshop, you can provide it by using an output section in the ARM template. The results can also be sent as email to the attendees when the template deployment is completed.  

### Creating and Managing ODL

- We will create an **ODL**
- Navigate to the portal using the link https://experience-azure-mgmt.azurewebsites.net/#/main and login with your AEC credentials.  
- Once logged in, click on **ODL** on the left pane of the portal. This will list the events if any.  

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/ODL_click.png"/>

- Click on **ADD ON DEMAND LAB** at the top right corner of the events page, to add a new event.  

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/Add_ODL.png"/>

- Now the Add ODL Details window comes up, where you can provide the following details.  
•	Name : Enter the Name of the ODL, which should be displayed on the ODL registration page.  
•	Template : Select the template which will be used to pre-deploy the resources required for the ODL.  
•	Description : Enter a description of the ODL which will be displayed on the ODL registration page as description.  
•	Tags : Enter tags such as Azure.  
•	Status : Choose one of the option to define the current status of the ODL.  
<br>a.	Registration Open : This defines that the registration for the ODL is open and users can register for the ODL.  
<br>b.	Registration Closed : This defines that the registration for the ODL is closed and users cannot register for the ODL. You can change the status of the ODL after the workshop is completed, confirm it onces a red strike is present over the ODL ID.  
•	Channels(optional) : Specify the channel to which the ODL belongs to.  
•	Approval : Choose one of the option to define the approval type for the ODL.  
<br>a.	Registration Required : This defines that the user should register for the ODL to get access to the ODL.  
<br>b.	Registration & Email Validation Required : This defines that the user should register for the ODL and launch the lab from the Email sent from AEC to get access to the ODL.  
<br>c.	Registration & Approval Required : This defines that the user should register for the ODL. Here the user will not be able to access the ODL unless the Instructor approves the registration from the User Window of the ODL.  
<br>d.	Invite Only : In this case the instructor can generate the vouchers to be distributed to the users, so that the users can use it to register the lab. The users cannot register without entering the voucher code asked in the registration page.  
•	Duration : Enter the duration that the lab environment should be available since its launch.  
•	Expiry Date : Choose a date from the calender, the ODL will be listed in the public till the date.  
•	Suscription Group : Choose the Azure subscription group to be used while deploying the resources required for the ODL.  
•	Licenses(optional) : Choose the license which you want to assign to the user for the lab.  
•	Custom ODL Page Title (optional) : Type in the text that you want to be displayed as the title of the ODL Registration Page.  
•	Video(optional) : Provide the link to video that you want the users to watch if registered for the video.  
•	Do Not Send Azure Credentials (optional) : Check this option if you do not want to send the Azure credentials to the users using the ODL.  
•	Is Private : Check this option if you do not want to show up this event on public pages. This can be checked for test or dry run events.  
•	Enable Vouchers(optional) : Check this option if you want to genete vouchers to distribute to the users. This will be checked by default if you select the approval type as Invite Only.  
•	Allow personal email addresses : Checking this option will allow sign up to the ODl from social accounts such as gmail,yahoo,etc, Business/Work emails address are always allowed.  
•	Allow USer to delete the ODL? : Check this option if you want to allow the users to delete the ODL after finishing the workshop.  
•	Enable Hot Instances : Check this option if you want to pre-deploy n number the deployments, so that the users needn't wait for the deployment to finish once they register and launch the lab. Once you enable this option it will ask for Minimum Available instances, which will not allow the instances to go below this number.  
•	Intelligence to self-heal : Check this option if you want to start another deployment for the failed hot instances and delete the failed ones.  
•	Test : Check this option if the ODL is for test purpose, so the it does not get extracted to the excel sheet.  

- Click on **Submit** once required options above are filled.

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/ODL_detail.png"/>
## ODL Hot Instance Management

a. Why Hot Instnaces - Hot Instance is used to pre-deploy the Lab environment even before the users register for the ODL. This is used to save the time of the users, they needn't wait for the pre-requisite template to deploy after launching the lab. If the hot instance is deployed early the users will immediately receive the lab details once they launch lab. The number of hot instance is deployed according to the number of registrations for the ODL.  
## Enable/Disable Hot Instances ##  
•	Click on **Edit Icon** to edit the created ODL.  

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/Edit_ODL.png"/>

•	Scroll down the Edit ODL page and check the option the corresponding to Enable Hot Instance  
•	This will ask the Minimum Available instances, where you can enter the minimum hot instances that is required at any point of time of the workshop. Once this is set the available hot instances will always be grater than or equal to this number.  
•	Click on **Submit** once required options above are filled.  

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/Enable-hot.png"/>

•	Enabling the Hot Instance in the Edit ODL page will create a new icon corresponding to the ODL.  
•	Click on **Check Hot Instance Icon** to edit the created ODL.  

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/Check_hot.png"/>

•	In the Hot Istance page, click on **ADD HOT INSTANCES** to deploy hot instnaces for the ODL.

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/Add_instances.png"/>

•	In the Add Hot instance Window that pops up, the Currently available hot instances show the instance which are availble, i.e unassigned to any user.  
•	In the Add Hot instance Window that pops up, enter the number of hot instance that you want to deploy, corresponding to the Number of Hot Instances test box.  
•	Click on **ADD** once required options above are filled.  

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/Number_instancepng.png"/>

c. Scheduling Hot Instances  
•	In the Hot Instance page, click on **ADD HOT INSTANCES** to schedule the deployment of hot instnaces for the ODL.  

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/Add_instances.png"/>

•	In the Add Hot instance Window that pops up, the Currently available hot instances show the instance which are availble, i.e unassigned to any user.
•	In the Add Hot instance Window that pops up, enter the number of hot instance that you want to deploy, corresponding to the Number of Hot Instances test box.  
•	Check the box corresponding to schedule, to schedule the deployment of Hot instances at a particular time.  
•	This will ask you the Time Zone, select the time zone of where the workshop is going to be held.  
•	Enter the time at which you want to start the deployment of hot instance.  
•	Click on **ADD** once required options above are filled.  

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/hot_schedule.png"/>

•	In the Hot Instance page, click on **SCHEDULES** to view the Hot Instance schedule history.  

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/click_schedule.png"/>

•	In the Hot Instance Schedules page, you can view all the schedules for the ODL. 

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/schedules_history.png"/>

•	In the Hot Instance Schedules page, you can also delete a schedule if you do not want to deploy the hot instance at scheduled time.  

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/schedule_delete.png"/>

### User ODL Management

 The ODL registration page looks as below  

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/ODL_reg.png"/>

**A** : The users can register for the workshop here with the required details and click on **Submit**.  
**B** : The name of the event is displayed here, which is same as the ODL name given at the time of ODL creation. It also shows the organisation which conducts the workshop with their Logo.  
**C** : This is the short description of the workshop, which is same as the description given at the time of ODL creation.  
**D** : This is the duration for which the user will have access to ODL environment.  
**E** : This is the email ID of the contact person who scheduled the workshop, which is same as given at the time of ODL creation.  
**F** : These are the tags mentioned while creating the ODL.  
**G** : This is the Custom ODL name that we mentioned at the time of ODL creation.  

- There are 4 type of user signup

a.	Registration Required : This defines that the user should register for the ODL to get access to the ODL.  
<br>b.	Registration & Email Validation Required : This defines that the user should register for the ODL and launch the lab from the Email sent from AEC to get access to the ODL.  
<br>c.	Registration & Approval Required : This defines that the user should register for the ODL. Here the user will not be able to access the ODL unless the Instructor approves the registration from the User Window of the ODL.  
<br>d.	Invite Only : In this case the instructor can generate the vouchers to be distributed to the users, so that the users can use it to register the lab. The users cannot register without entering the voucher code asked in the registration page.  

- Registration Management

-Navigate to the portal using the link https://experience-azure-mgmt.azurewebsites.net/#/main and login with your AEC credentials.  
-Once logged in, click on **ODL** on the left pane of the portal. This will list the ODLs if any.
   
 <img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/ODL_click.png"/> 
  
-Click on **Edit Icon** to edit the created ODL.  

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/Edit_ODL.png"/>

-In the Edit ODL page, copy the URL from the first field. This is the ODL registration page URL. The Instructor can customize this URL using bitlink before 

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/ODL_URL.png"/>

### Managing and distributing Voucher’s

-Navigate to the portal using the link https://experience-azure-mgmt.azurewebsites.net/#/main and login with your AEC credentials.

-Once logged in, click on On Demand labs on the left pane of the portal. This will list the all ODL's if any.

<kbd><img src="/Images/Vouchers_odl.png"/></kbd>

-Navigate Test ODL that created earlier, Click on Edit Icon to edit the created ODL.For create voucher, approval will be Invite only.
* Approval : Choose only **invite only** option to define the approval type for the ODL.

-Invite Only : In this case the instructor can generate the vouchers to be distributed to the users, so that the users can use it to register the lab. The users cannot register without entering the voucher code asked in the registration page.

* Enable Vouchers : Check this option if you want to genete vouchers to distribute to the users. This will be checked by default if you select the approval type as Invite Only.

-Click on **Submit** once required options above are filled.

<kbd><img src="/Images/Click_EnableVoucher.png"/></kbd>

-click on **Vouchers** button.

<kbd><img src="/Images/Click_VoucherButton.png"/></kbd>

-Click on **Add Vouchers**.

<kbd><img src="/Images/Click_AddVouchers.png"/></kbd>

-Now provide the following details in the Add Vouchers Page that comes up.

<kbd><img src="/Images/Click_Submit.png"/></kbd>

-Now you can see the voucher added successfully.

<kbd><img src="/Images/Vouchers_addedSuccessfully.png"/></kbd>

The ODL registration page looks as below.

<kbd><img src="/Images/Registration_Page.png"/></kbd>

-The users can register for the workshop here with the required details and click on Submit.

* There are 4 type of user signup.

a. Registration Required : This defines that the user should register for the ODL to get access to the ODL.

b. Registration & Email Validation Required : This defines that the user should register for the ODL and launch the lab from the Email sent from AEC to get access to the ODL.

c. Registration & Approval Required : This defines that the user should register for the ODL. Here the user will not be able to access the ODL unless the Instructor approves the registration from the User Window of the ODL.

d. Invite Only : In this case the instructor can generate the vouchers to be distributed to the users, so that the users can use it to register the lab. The users cannot register without entering the voucher code asked in the registration page.

### Distributing Vouchers
-Copy the Voucher Code that you created and give in registration page.

<kbd><img src="/Images/Copy_VoucherCode.png"/></kbd>

-paste the Voucher Code in Registration page below.

<kbd><img src="/Images/Registration_Add%20details.png"/></kbd>

-Click on **Submit** once required options are filled.

-Now you can see the registration successful.

<kbd><img src="/Images/Registration_Successfull.png"/></kbd>

-Navigate to the portal using the link https://experience-azure-mgmt.azurewebsites.net/#/main and login with your AEC credentials.

-Once logged in, click on On Demand labs on the left pane of the portal. This will list the all ODL's if any.

-Click on Vouchers Button.

-Now Click on **Available** button, you can see the voucher code that is available for user.

<kbd><img src="/Images/Click_Available.png"/></kbd>

-Now click on **Redeemed** button, you can see that voucher code is redeem for user.

<kbd><img src="/Images/Click_Redeemed.png"/></kbd>
  
### Creating and Managing Event

The event registration page looks as below  

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/event-registration-page.png"/>

**A** : The users can register for the event here with the required details and click on **Submit**.  
**B** : The name of the event is displayed here, which is same as the event name given at the time of event creation.  
**C** : This is the short description of the event, which is same as the description given at the time of event creation.  
**D** : This is the date at which the event is scheduled, which is same as the date given at the time of event creation.  
**E** : This is the time and time zone at which the event is scheduled, which is same as the time given at the time of event creation.  
**F** : This shows that the event will be held online. An event type can be either Online or In person depending on the choice we provide at the time of event creation. If we choose In person option, the address at which the event will be held will be displayed here.  
**G** : This is the language in which the event will be held, which is same as the language choose at the time of event creation.  
**H** : This is the email ID of the contact at which the event is scheduled, which is same as given at the time of event creation.  
**I** : Clicking on this will take you back to Events calendar.  

- Now we will create an **Event**
- Navigate to the portal using the link https://experience-azure-mgmt.azurewebsites.net/#/main and login with your AEC credentials.  
-Once logged in, click on **Events** on the left pane of the portal. This will list the events if any.  

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/select-event.png"/>

-Click on **ADD** at the top right corner of the events page, to add a new event.  

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/add-event.png"/>

- Now the Add Event Details window comes up, where you can provide the following details.  
•	Event Title : Enter the Name of the event, which should be displayed on the event registration page.  
•	Template : Select the template which will be used to pre-deploy the resources required for the workshop.    
•	Description : Enter a description of the event which will be displayed on the event registration page as description.  
•	Tags(optional) : Enter tags such as Azure, checkpoint. Not being used as of now  
•	Event Type : Choose either of the following type  
	Virtual : Choose this type when the event is to be conducted online  
   <br>a.	Link to online meeting : Provide a link on which the Attendees can join the event  
	In Person : Choose this type when the event is to be conducted offline  
   <br>a.	Address : Enter the required details so that the Attendees gets to know where the event is held. It will be displayed on the event registration page.  
•	Sponser(optional) : Choose the sponser of the event from the list.    
•	Channels(optional) : Specify the channel to which the event belongs to.   
•	Email Template : Choose the template for emails sent out to event participants. This template defines the structure and content of the emails.  
•	Suscription Group : Specify the Azure subscription detail to be used while deploying the resources required for the event.    
•	Is Private : Check this option if you do not want to show up this event on public pages. This can be checked for test or dry run events.  
•	Time Zone : Scroll and select the time zone from where you are setting up the event. This will be displayed on the event registration page.    
•	Start Date and Start Time : Specify Start date and time of the event.  This will be displayed on the event registration page.    
•	End Date and End Time : Specify end date and expected time on which the event will end. This will be displayed on the event registration page.    
•	Approval Type : Specify how the participant registrations should get approved  
	Manual : Will have to manually approve participant registrations.  
	Automatic : Will automatically approve the registration until the total limit is met.  
•	Maximum number of users : Define the maximum number of participants for the event. Any registration after reaching this number would be marked in waitlist category.  
•	Allow personal email addresses : Checking this option will allow sign up to the event from social accounts such as gmail,yahoo,etc, Business/Work emails address are always allowed.  
•	Contact Email : Specify the email address that will appear on the event registration page for any support/questions about the event.  
•	Survey URL(optional) : This is to collect feedback post event, you can leave this blank to start with and enter survery url later on if required.  This will be sent to participants in thank you email after the completion of event.  
•	Recorded Session URL(optional) : Provide the link to recorded session. you can leave this blank to start with and enter survery url later on if required. You can choose to send this to participants after training.  
•	Language(optional) : Specify the language to be used in workshop. This will be displayed on the event registration page.    
•	Additional Notes(optional) : Type in additional notes if any, which will be shown on the public event page.  
•	Schedule Remainder Email : Check the options below to send event remainder email automatically.  
	Before Two Weeks  
	Before Two Days  
	Before Two Hours  
  Click on Submit.  

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/event-creation.png"/>

-Now you can see the event that you just created, in the Event page.  

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/event-list.png"/>

### Archieve an Event

Navigate to the portal using the link https://experience-azure-mgmt.azurewebsites.net/#/main and login with your AEC credentials.  
-Once logged in, click on **Events** on the left pane of the portal. This will list the events if any.  

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/select-event.png"/>

-Now click on **Archive** icon coreesponding to the evnet you want to archive.  

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/archive-event.png"/>

-Now you can find the archived event by clicking on **Archived Events** options at top right corner of events page.  

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/Archive-list.png"/>

### Manage Registrations


-Now we will **Approve/Reject** the attendees registration from AEC portal.  
-Navigate to the portal using the link https://experience-azure-mgmt.azurewebsites.net/#/main and login with your AEC credentials.  
-Once logged in, click on **Events** on the left pane of the portal. This will list the events if any.  

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/select-event.png"/>

-Now click on **Manage this event**  button corresponding to your event, in the Events Page.

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/open-event-settings.png"/>

-Now inside event page, scroll down and under the registration section, click on **Manage Attendees**.

## Report
## Dashboard Overview
<kbd><img src="/Images/ODL_Dashboard.png"/></kbd>

-In Dashboard Overview Section, you can see the **12 ODLs** and **30 Attendees**.
<kbd><img src="/Images/ODL%26Attendees.png"/></kbd>

-In Dashboard Section, you can filter by date. Click on this button.

<kbd><img src="/Images/Filter_by_date.png"/></kbd>

-Click on calendar button

<kbd><img src="/Images/Filter_by_date1.png"/></kbd>

-Click **OK**.

<kbd><img src="/Images/filter_by_date2.png"/></kbd>

-In Dashboard Section, Click on **Export all** Button. It will directly download the excel sheet  Report of all data.

<kbd><img src="/Images/Click_ExportAll.png"/></kbd>

<kbd><img src="/Images/Exportall_Report.png"/></kbd>

-In Dashboard Section, you can see the 
* METRICS BY ATTENDEE COUNT
* METRICES BY TEMPLATE
* METRICES BY ORGANIZATION
* METRICES BY COUNTRY

### METRICS BY ATTENDEE COUNT
-In Metrices by Attendee count,you can see all attendees of ODLs. For Export Report Click on **Export** button. it will directly download the excel sheet of the report.

<kbd><img src="/Images/Metrices_AttendeeCount.png"/></kbd>

<kbd><img src="/Images/Attendee_ExportReport.png"/></kbd>

### METRICES BY TEMPLATE
-In Metrices by template, you can see all templates. For Export Report Click on **Export** button. it will directly download the excel sheet of the report.

<kbd><img src="/Images/Metrices_TemplateCount.png"/></kbd>

<kbd><img src="/Images/Template_ExportReport.png"/></kbd>

### METRICES BY ORGANIZATION
In Metrices by organization, you can see all Organizations. For Export Report Click on **Export** button. it will directly download the excel sheet of the report.

<kbd><img src="/Images/Metrices_Organization.png"/></kbd>

<kbd><img src="/Images/Organization_ExportReport.png"/></kbd>

### METRICES BY COUNTRY
In Metrices by Country, you can see all Country. For Export Report Click on **Export** button. it will directly download the excel sheet of the report.

<kbd><img src="/Images/Metrices_Country.png"/></kbd>

<kbd><img src="/Images/Country_ExportReport.png"/></kbd>

## License Key Distribution

### How to Create license key
-Navigate to the portal using the link https://experience-azure-mgmt.azurewebsites.net/#/main and login with your AEC credentials.  
-Once logged in, click on **License key** on the left pane of the portal. This will list the Licenses if any. 

<kbd><img src="/Images/License_key.png"/></kbd>

-Click on ADD at the top right corner of the License page, to add a new License Type.

<kbd><img src="/Images/Click_Add_LicenseType.png"/></kbd>

-Now provide the following details in the Add License type page that comes up.
* Name : Provide a suitable name to the License type

-Click on Submit once required options are above filled.

<kbd><img src="/Images/Create_LicenseKey.png"/></kbd>

-Click on Action Button to add the License.

<kbd><img src="/Images/License_Action.png"/></kbd>

-Click on Add License.

<kbd><img src="/Images/Click_AddLicense.png"/></kbd>

-Now provide the following details in the Add license page that comes up.
* License type: Choose the License which you created before.
* Expiry Date: Choose any suitable date.
* Licenses: Provide any suitable name for License.
* License Cost: Provide cost of the License.

<kbd><img src="/Images/Click_Add_LicenseDetails.png"/></kbd>

-Click on Submit once required options are above filled.



<!-- /TOC -->
