Send emails with attachments to external users
##############################################

This article will describe the advanced features of our `Send e-mail with attachments </workflow-actions-pack/docs/>`_ workflow actions. This approach works for SharePoint 2013 / 2016 as well as for SharePoint Online in Office 365.

Table of Contents
*****************


*  `SMTP VS Exchange version <#SMTPVSExchange>`_ 
*  `How to get attachment URLs from current list item <#GetAttachments>`_ 
*  `How to specify multiple recipients (To, CC, BCC, ReplyTo fields) <#MultipleRecipients>`_ 
*  `How to setup complex message formatting <#ComplexFormat>`_ 
*  `How to embed images into message body <#EmbedImages>`_ 



SMTP VS Exchange version
************************
First, the difference between `SMTP </workflow-actions-pack/docs/email-processing/#SmtpSendEmail>`_ and `Exchange </workflow-actions-pack/docs/email-processing/#SendEmail>`_ versions. Indeed they works similarly and the only difference that they use different protocols. The Exchange version uses Exchange Web Services Protocol (EWS), also it uses auto discoverer to find the right mail server. The SMTP version uses standard SMTP protocol to send your email. Unfortunately, auto discover service of SharePoint Online is not stable and sometime doesn’t discover correct address. Our workflow action is smart enough to detect such cases and retry auto discover, but sometime it doesn’t help. We recommend you to use SMTP version (Exchange allows sending messages through SMTP). But if you have any difficulties with SMTP you still can use Exchange version.

How to get attachment URLs from current item
********************************************
When you are configuring Send Email workflow action, you might need to specify attachment URLs. If you create a list level workflow, you can use `Get Attachments to Dictionary </workflow-actions-pack/docs/documents-list-items-processing/#GetAttachments>`_ in conjunction with `Join Dictionary Values </workflow-actions-pack/docs/string-processing-workflow-actions/#DynamicValueJoinToString>`_ to get attachments from current item (or any Item by ID) into array and join it into the string. You have to join to string to create correct semicolon delimitated list of URLs. The example of use you can see at figure below:


.. image:: /_static/img/send-email-with-attachments-1.png
   :alt: SharePoint get current item attachment links

How to specify multiple recipients or Reply mailbox (To, CC, BCC, ReplyTo fields)
*********************************************************************************
Using advanced properties you can fill in additional fields. In addition, you can specify multiple fields using semicolon (‘;’) as separator.


.. image:: /_static/img/send-email-with-attachments-2.png
   :alt: Send email to multiple receipients

How to setup complex formatting
*******************************
The workflow actions support HTML in the message body . You can use any HTML tags with style attributes to format you email message. As example, I provide open source `Responsive HTML Email Template <https://github.com/leemunroe/responsive-html-email-template>`_ .


.. image:: /_static/img/send-email-with-attachments-3.png
   :alt: SharePoint Workflow Email HTML template
 
How to embed images into text
*****************************
You can specify “Parse Images” option in workflow action properties. Once you did it, the email body will be parsed (it will try to parse all img tags). The workflow action will download all images and include it as embed images. Note, you can embed images located inside SharePoint site. The workflow action can’t embed images from other sources.


.. image:: /_static/img/send-email-with-attachments-4.png
   :alt: SharePoint Workflow Send Embed Images

