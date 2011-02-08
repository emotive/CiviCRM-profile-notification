/*****************************************
 * CiviCRM Profile Notification Module
 * by Chang Xiao (chang@emotivellc.com)
 * EMotive LLC, 2010
 * GNU GENERAL LICENSE - see LICENSE.txt
 ****************************************/
 
 ----------------------------------------
 Description
 ----------------------------------------
 This is a module that will allow a notification email
 TO THE PERSON who filled out the profile form.
 
 It is DIFFERENT than the profile notification feature from
 CiviCRM, which sends a notification email to the administrator
 when someone fills out a profile form.
 
 
1. Requirements
2. Installation
3. Configuration 
4. Usage
5. Future considerations
6. Change log

/*************************************************************
 * 1. Requirements
 ************************************************************/
 
This module requires the following:
 
	1. Drupal Version 6.x
	2. CiviCRM 3.x (Versions with API V2)
	3. *Your Drupal and CiviCRM needs to be in the same database*
	4. Able to send email with mail() function
	(You can also install drupal SMTP authentication module 
	to bypass this requirement)

/*************************************************************
 * 2. Installation 
 ************************************************************/	

 The following steps are needed to make the module work:
 
	1. Upload all the contents in the civicrm_profile_notificiation folder to your drupal 
	sites/all/modules/ folder.
	
	2. Enable the module "CiviCRM profile notification" from admin/build/modules
	
	3. Configure the module from admin/settings/civicrm_profile_notification

/*************************************************************
 * 3. Configuration
 ************************************************************/		
	
	1. email template to use:
	
	Select the email template to use for the notification email,
	the email templates are from
	civicrm/admin/messageTemplates&reset=1
	
	under user-driven templates
	
	!!!!! IMPORTANT !!!!!
	In the message template you have selected, you must enter the token
	
	{content}
	
	Otherwise the template will not be brought in the notification email.
	
	2. For each of the profile that is type (individual), you can enter
	the subject of the email and the email body. Email body conforms to
	the filtered html input type in Drupal.
	
	By default, the profile notification is off for all profiles.
	
	The email will come from whatever the setting you have for site email in the drupal configuration settings.
	

/*************************************************************
 * 4. Usage
 ************************************************************/	

	Notification email will be sent whenever someone fills out
	a profile form that has notification enabled.


/*************************************************************
 * 5. Future Consideration
 ************************************************************/
 
	1. Use CiviCRM DAO for database query
	2. Merge this into CiviCRM Core
	
	If you have other ideas and suggestions, please contact at chang@emotivellc.com
	and feel free to contribute to the code
	
/*************************************************************
 * 6. Change log
 ************************************************************/
 
1.0 Working Version: 2/8/2011