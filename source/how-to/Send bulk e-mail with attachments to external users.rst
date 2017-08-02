Send bulk e-mail with attachments to external users
###################################################

This article will show how to configure SharePoint 2013/Online workflow to send bulk email with attachments to external users using SharePoint 2013/Online workflow. For many business tasks it is required to send mass messages to customers or employees. Sometimes such messages has to contain attachments.There are multiple use cases, look at just a few of them:


* To send information about new releases to customers.
* To notify customers about upcoming downtime.
* To send documents for external users as attachments for approval.
* To send corporate newsletter to external and internal subscribers as PDF attachment.

It will show how to send corporate newsletter as PDF attachment to list of subscribers, but you can use my approach for any other mass mailing system.

It will create SharePoint document library to store PDF files, then I will create SharePoint list to store information about subscribers. Then I will configure SharePoint workflow to send messages. Finally I will show how to add custom menu item into document library’s context menu. This menu item will be used to start the notification workflow.

As result end user will have to select document and click ‘Send to subscribers’ to send bulk e-mail to all subscribers:


.. image:: /_static/img/bulk-email-attachments-1.png
   :alt: 


Finally there's the following steps:



1. To create SharePoint list to store subscribers and document library to store corporate newsletter files
2. To configure workflow for notifications:
3. To configure workflow action to get recipients from SharePoint list by CAML query
4. To configure workflow action to send current document as attachment to subscribers
5. To create custom menu item to start workflow manually

It will need to query all subscribers from list of subscribers using CAML query, then iterate through the list of subscribers and sent messages with attachments. SharePoint 2013 provides two types of workflows: SharePoint 2013 workflows (WF 4.5) and SharePoint 2010 workflows (WF 3.5). The best choice for us is SharePoint 2013 workflow, because it allows to use loops and we need loop to iterate through the list of our subscribers.

Out of the box workflow actions don’t provide required functionality. It will use two workflow actions from paid `Workflow Actions Pack <http://plumsail.com/workflow-actions-pack/>`_ which allow to query list items using CAML query and to send e-mails with attachments to external user:



*  `Get items by query <http://plumsail.com/workflow-actions-pack/docs/actions-description/#GetItems>`_ 
*  `Send e-mail with attachment (SMTP) <http://plumsail.com/workflow-actions-pack/docs/actions-description/#SmtpSendEmail>`_ 


You can also use `Send e-mail with attachment (Exchange) <http://plumsail.com/workflow-actions-pack/docs/actions-description/#SendEmail>`_ .

How to create list of subscribers and document library
------------------------------------------------------
To store subscribers it was created new SharePoint list and named it ‘Maillist’. The structure of the list is quite simple:


.. image:: /_static/img/bulk-email-attachments-2.png
   :alt: 


It was added only one text column ‘E-mail’. Internal name of this field is ‘EMail’. You can create any additional columns, for example check box to unsubscribe. Then you can use it in the CAML query to exclude users from notification.

This is how my list of subscribers looks:


.. image:: /_static/img/bulk-email-attachments-3.png
   :alt: 


To store files of corporate newsletter I created document library and named it ‘Corporate newsletter’. It didn’t create any additional columns.

This is structure of lists and libraries with internal names and URLs:

*Maillist*  – Generic SharePoint list to store e-mail addressesUrl: /Lists/MailingListAdditional columns: Email – single line of text

*Corporate newsletter*  – Document library to store files of corporate newsletter.URL: /CorporateNewsletter

How to configure workflow to send bulk e-mail
---------------------------------------------
If one wants to send notifications for each corporate newsletter file separately, that is why it was created list level workflow for ‘Corporate newsletter’ document library. This workflow will be executed on newsletter file and send this file as attachment to all subscribers from the ‘Maillist’.

This is how the workflow looks:


.. image:: /_static/img/bulk-email-attachments-4.png
   :alt: 


To reproduce this workflow you need to know names of workflow variables with types:


.. image:: /_static/img/bulk-email-attachments-5.png
   :alt: 

In the first stage it initializes credentials. It will use them for SMTP settings. It also needs credentials for SharePoint Online to query list by CAML. Workflow action for SharePoint 2013 on-premise doesn’t require credentials to query list items.

Then it uses *Get items by query*  workflow action to get all subscribers. Next, it counts subscribers and initialize index. I need to count subscribers to configure loop. The index is required to get subscriber by index withing loop.

Then it uses loop to iterate through subscribers. It uses out of the box *Get an item from a Dictionary*  workflow action to get e-mail of current subscriber by index. Then I send e-mail to subscriber using *Send e-mail with attachment (SMTP)*  workflow action. Finally I increment the index.

It was described logic of workflow step by step. Now let me show how individual workflow actions are configured.

Get items by query workflow action configuration
++++++++++++++++++++++++++++++++++++++++++++++++
This is how the workflow action is configured:

*List:*  Maillist. *Save result items to variable:*  ‘Recepients’. *Caml query:* 

| <View>
|   <Query>
|     <Where>
|     </Where>
|   </Query>
|   <ViewFields>
|     <FieldRef Name="EMail" />
|   </ViewFields>
| </View>

As you see it was used quite simple CAML query ‘’, it doesn’t contain any conditions. It was used such query because I don’t need to filter exclude subscribers from the list. I want to notify all of them, but feel free to add conditions in this query. For example you can add ‘Unsubscribe’ column into the list of subscribers and add condition into this query to exclude such subscribers.

Also look at section. It was added EMail column into view fields. This allows to get value of EMail column from results of query.

*Get an item from a Dictionary workflow action configuration*

The result or query will be stored in the variable ‘Recepients’. This is not obvious, but dictionary in SharePoint workflow can store collection of elements not only key value pairs.\To access single e-mail from collection of e-mails I use *Get an item from a Dictionary*  workflow action. This is how the workflow action is configured:

*Path:*  ([%Variable: LoopIndex%])/FieldValues/EMail *Save result to variable:*  ‘Recepient’

As you can see it was composed the path dynamically based on the current index within loop. It will get item from collection of subscriber by index using this path. EMail here is an internal name of the column. If you use other column, replace it with internal name of your column.



Send e-mail with attachment workflow action configuration
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++
Great, now we have recipient. The next step is to send e-mail.

Firstly it configures general settings.

It uses variable ‘Recepient’ as e-mail address. It was also specified some subject and body. Then SMTP settings, you need to specify settings for your account.

To attach files I added link into AttachmentsUrls property. Look at the picture below for details:

 
.. image:: /_static/img/bulk-email-attachments-6.png
   :alt: 

For SharePoint Online it is also required to specify AdminLogin and AdminPassword properties. SharePoint 2013 on-premise doesn’t require it.

That is all. The workflow is ready to send notifications based on mailing list.

How to create menu item for document library to start workflow manually
-----------------------------------------------------------------------
In the beginning of this article it was mentioned that end user will be able to send notifications using context menu of the file. It looks like this:


.. image:: /_static/img/bulk-email-attachments-7.png
   :alt: 

To add custom action for document context menu you need to open ‘Corporate newsletter’ document library using SharePoint Designer. Select ‘Custom Actions’ section and click ‘Custom action -\>List Item Menu’ in the ribbon. Then configure workflow action to initiate workflow:


.. image:: /_static/img/bulk-email-attachments-8.png
   :alt: 

