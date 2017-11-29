Version history
==================================================


2.10
--------------------------------------------------
* New workflow action Add Content Type to List
* New workflow action Check In Document 
* New workflow action Check Out Document
* New workflow action Convert HTML to PDF and Save as Attachment 
* New workflow action Convert HTML to PDF and Save as Attachment in Current Item 
* New workflow action Copy List Item to List
* New workflow action Move List Item to List
* New workflow action Copy Current List Item to List
* New workflow action Move Current List Item to List
* New workflow action Get Items from View
* New workflow action HTML Encode
* New workflow action Invite External Users
* Old workflow action Invite External Users renamed to Invite External Users to Group
* New workflow action Share the Item


2.9
--------------------------------------------------
* Add workflow actions to work with Document Sets (Copy / Move)
* Add workflow action to remove document 
* Rewrite workflow actions for work with copy / move files / folders
* Add additional parameter "PaperSize" to Convert HTML to PDF workflow action 
* Add workflow action Get Version 
* Simplify Send an Email workflow action (reduce cound of requred parameters)
* Add workflow action Create Folder by URL
* Add workflow action Increment value
* Add workflow action Build Dictionary from JSON


2.8
--------------------------------------------------

* Now you can manage credentials for workflow actions in site level settings.
* Bug fix for Get Items by Query, it worked at current site only
* New workflow action Get Items by Query (Many Lists)
* New workflow action Invite External Users
* New workflow action Activate Feature
* New workflow action Set Up Default Group for the Site

.. warning::
	Important Upgrade Note 
	Please `read this blog article <https://plumsail.com/blog/2014/12/store-credentials-at-site/>`_ to get more information about upgrade.

2.7
--------------------------------------------------

* New workflow action Delete Site
* New workflow action Evaluate expression
* New workflow action Create List Item at Any Site
* New workflow action Update List Item at Any Site

2.5
--------------------------------------------------

* New workflow action Convert HTML to PDF
* New workflow action Sync Mailbox with List (Shared mailbox). Now you can sync site mailbox with custom list
* New workflow action Start a Site Workflow
* New workflow action Start a List Workflow
* Changed workflow action Get Items by Query, now it supports cross-site. We also added new output parameter count items
* Added new parameter ‘Group owner’ for workflow action Create SharePoint Group

.. warning::
	We added cross-site support to Get Items by Query workflow action. If you used it in your workflows you need to manually update it within your workflows after solution upgrade. Please follow the upgrade guide, then open your existing workflows in the SharePoint Designer. Find all ‘Get Items by Query’ workflow actions and specify value for  ‘List URL’  property. Then publish the workflow.

2.4
--------------------------------------------------

* New workflow action Render Text Template
* New workflow action Regular Expression Match
* New workflow action Regular Expression Replace
* New workflow action Regular Expression Test

2.1
--------------------------------------------------
* Added new set of workflow actions Azure AD Administration
* Added ‘File processing’ workflow actions set
* Renamed mostly of workflow actions, now it is more simple to use
* Added intelegent resolving for most parameters

2.0
--------------------------------------------------
* Added new set of workflow actions Documents and list items processing
* Rewrited internal engine
* Added new workflow actions
* Implemented workflow upgrade logic

1.5
--------------------------------------------------
* Added free set of workflow actions String Processing (Free)
* Minor bug fixes

1.0
--------------------------------------------------
* Added new set of workflow actions E-mail processing
* Added new set of workflow actions Permissions management
* Added new set of workflow actions Social integration
* Added new set of workflow actions SharePoint Administration