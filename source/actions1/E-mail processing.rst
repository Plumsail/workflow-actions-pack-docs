E-mail Processing
==================================================
Workflow actions to work with email, it allows you send and receive the emails.


Sync Mailbox with List (Exchange)
--------------------------------------------------
Synchronizes unread messages from a specific Exchange account with a SharePoint list.

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  Email
       -  E-mail of the Exchange User
       -  support@contoso.com
    *  -  Password
       -  Password of Exchange User
       -  Support’sP@ssw0rd$
    *  -  List
       -  SharePoint List for synchronization. 
          The following fields will be filled from e-mail automatically: 

          * **From**, **To**, **Subject** (type: Single line of text) 
          * **Body** (type: multiline of text)
       -  Tickets
    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn’t exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn’t exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  SharePoint URL, if blank will be detected automatically
       -  empty
    *  -  mTo
       -  Specifies mapping of 'To' filed to list item field
       -  To
    *  -  mFrom
       -  Specifies mapping of 'From' filed to list item field
       -  From
    *  -  mSubject
       -  Specifies mapping of 'Subject' filed to list item field
       -  Title
    *  -  mBody
       -  Specifies mapping of 'Body' filed to list item field
       -  Body
    *  -  RegexTemplate
       -  Specifies regular expression template which allows to add new messages to existing discussion according to subject. This property is used for discussion boards only.
       -  ``Ticket#(? \d+)``
    *  -  SyncAttachments
       -  Synchronize e-mail messages with attachments
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/SyncExchangeEmails.png
   :alt: Sync Exchange Emails to SharePoint

Sync Mailbox with List (IMAP)
--------------------------------------------------
Synchronizes unread messages from a specific IMAP account with a SharePoint list.

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  Email
       -  Mailbox for sync
       -  support@contoso.com
    *  -  Password
       -  Password for Mailbox
       -  Support’sP@ssw0rd$
    *  -  List
       -  SharePoint List for synchronization. 
          The following fields will be filled from e-mail automatically: 

          * **From**, **To**, **Subject** (type: Single line of text) 
          * **Body** (type: multiline of text)
       -  Tickets
    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn’t exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn’t exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  Host
       -  IMAP Server name
       -  outlook.office365.com
    *  -  Port
       -  IMAP Port
       -  993
    *  -  SSL
       -  Is encryption required? (SSL or TLS)
       -  Yes
    *  -  SiteUrl
       -  SharePoint URL, if blank will be detected automatically
       -  empty
    *  -  mTo
       -  Specifies mapping of 'To' filed to list item field
       -  To
    *  -  mFrom
       -  Specifies mapping of 'From' filed to list item field
       -  From
    *  -  mSubject
       -  Specifies mapping of 'Subject' filed to list item field
       -  Title
    *  -  mBody
       -  Specifies mapping of 'Body' filed to list item field
       -  Body
    *  -  RegexTemplate
       -  Specifies regular expression template which allows to add new messages to existing discussion according to subject. This property is used for discussion boards only.
       -  ``Ticket#(? \d+)``
    *  -  SyncAttachments
       -  Synchronize e-mail messages with attachments
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/SyncIMAPEmails.png
   :alt: Sync Mailbox to SharePoint via IMAP

Sync Mailbox with List (Shared Mailbox)
--------------------------------------------------
Synchronizes unread messages from the SharePoint shared mailbox with a list.
Note: This action is accessible only for SharePoint Online.

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  Mailbox
       -  E-mail of the SharePoint online shared mailbox
       -  SMO-Main@plumsail.com
    *  -  List
       -  SharePoint List for synchronization. 
          The following fields will be filled from e-mail automatically: 

          * **From**, **To**, **Subject** (type: Single line of text) 
          * **Body** (type: multiline of text)
       -  Tickets
    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn’t exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn’t exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  SharePoint URL, if blank will be detected automatically
       -  empty
    *  -  mTo
       -  Specifies mapping of 'To' filed to list item field
       -  To
    *  -  mFrom
       -  Specifies mapping of 'From' filed to list item field
       -  From
    *  -  mSubject
       -  Specifies mapping of 'Subject' filed to list item field
       -  Title
    *  -  mBody
       -  Specifies mapping of 'Body' filed to list item field
       -  Body
    *  -  RegexTemplate
       -  Specifies regular expression template which allows to add new messages to existing discussion according to subject. This property is used for discussion boards only.
       -  ``Ticket#(? \d+)``
    *  -  SyncAttachments
       -  Synchronize e-mail messages with attachments
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/ExchangeRestToSP.png
   :alt: Sync SharedMailbox to SharePoint

Send E-Mail with Attachments
--------------------------------------------------
Send an e-mail with attachments. If the option AddItemAttachments is checked, a workflow will send attachments from the current list item or a document set. Alternatively you can turn on parsing links of documents from the message body or fill in parameter "AttachmentUrls".

.. note::
   If you use Office 365, to enable sending attachments you also need to specify AdminLogin and AdminPassword properties or setup it via `credential management page <https://plumsail.com/blog/2014/12/store-credentials-at-site/>`_.
   If you don't specify them, the workflow action will not be able to access your attachments.

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  To
       -  E-mail of the recipient
       -  SomeUser@gmail.com
    *  -  Subject
       -  Subject of the message
       -  SharePoint notification
    *  -  Body
       -  Body of message (may contain HTML)
       -  ``<h1>Approve notification</h1> <p>Dear Mr....</p>``
    *  -  Add Item Attachments
       -  If the option is checked, a workflow will send attachments from the current list item or a document set.
       -  True
    *  -  FromDisplayName
       -  You can change a display name of the From header
       -  Plumsail notification system
    *  -  Email
       -  E-mail that is used to connect to the SMTP server
       -  support@contoso.com
    *  -  Password
       -  Password to connect to SMTP server
       -  Support’sP@ssw0rd$
    *  -  Host
       -  SMTP Server name
       -  outlook.office365.com
    *  -  Port
       -  SMTP Port
       -  587
    *  -  SSL
       -  Is encryption required? (SSL or TLS)
       -  Yes
    *  -  ReplyTo
       -  Address for reply
       -  no-reply@plumsail.com
    *  -  ParseLinks
       -  Search embedded links in the message body
       -  False
    *  -  ParseImages
       -  Search for embedded images in the message body
       -  False
    *  -  AttachmentUrls
       -  Urls of attachments delimited by ';'
       -  /somefolder/sometxt.txt;http://somesite.com/images/someimage.img
    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn’t exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn’t exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  SharePoint URL, if blank will be detected automatically
       -  empty


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/SendEmail.png
   :alt: Send email with attachments

