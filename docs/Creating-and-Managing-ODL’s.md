## Creating and Managing ODL’s
 * [ODL Create](#odl-create)
   * [Explanation of all field’s](#explanation-of-all-field’s)
 * [ODL Hot Instance Management](#odl-hot-instance-management) 
   * [Why and How of Hot Instances](#why-and-how-of-hot-instances)
   * [Enable/Disable Hot instances](#enable/disable-hot-instances)
   * [Scheduling Hot Instances](#scheduling-hot-instances)

### ODL Create
- We will create an **ODL**
- Navigate to the portal using the link https://experience-azure-mgmt.azurewebsites.net/#/main and login with your AEC credentials.  
- Once logged in, click on **ODL** on the left pane of the portal. This will list the events if any.  

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/ODL_click.png"/>

- Click on **ADD ON DEMAND LAB** at the top right corner of the events page, to add a new event.  

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/Add_ODL.png"/>

- Now the Add ODL Details window comes up, where you can provide the following details
### Explanation of all field’s
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

### ODL Hot Instance Management
a. Why Hot Instnaces - Hot Instance is used to pre-deploy the Lab environment even before the users register for the ODL. This is used to save the time of the users, they needn't wait for the pre-requisite template to deploy after launching the lab. If the hot instance is deployed early the users will immediately receive the lab details once they launch lab. The number of hot instance is deployed according to the number of registrations for the ODL.  

### Enable/Disable Hot Instances   
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

### Scheduling Hot Instances  
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

