## Creating AEC Templates
  * [Create Template](#create-template)
    * [Explanation of all fields](#explanation-of-all-fields)
  * [ARM Template Best Practices](#arm-template-best-practices)
    * [Use of template outputs](#use-of-template-outputs)
  * [Template Permissions](#template-permissions)
    * [Explanation with details to implement](#explanation-with-details-to-implement)
  * [Validating Template](#validating-template)
    * [Validation](#validation)
    
 ### Create Template
-Navigate to the portal using the link https://experience-azure-mgmt.azurewebsites.net/#/main and login with your AEC credentials.  
-Once logged in, click on **Templates** on the left pane of the portal. This will list the templates if any.  

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/templates.png"/>

-Click on **ADD** at the top right corner of the templates page, to add a new template.  

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/add_template.png"/>

-Now provide the following details in the Add Template page that comes up.  
### Explanation of all fields
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

### ARM Template Best Practices
### Use of template outputs
-If you want to provide the attendees some results that are required in the workshop, you can provide it by using an output section in the ARM template. The results can also be sent as email to the attendees when the template deployment is completed.  

### Template Permissions

-Click on **Edit Icon** to edit the created template and add the template permissions if any

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/Template_Edit.png"/>

### Explanation with details to implement 
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

### Validating Template
### Validation
-Click on **Validate subscription with ARM template** icon corresponding to the template created.  

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/Template_validate.png"/>

-Provide the azure subscription group and subscription in which the validator should be run. Also provide the regions where you want to validate the template and click on **Submit**.  

<img src="https://github.com/Suraj2093/Azure-Experience-Centre/blob/master/Images/validation_details.png"/>

