How to check-in multiple files
##############################

This article explains how to check-in multiple documents. This approach works in SharePoint 2013 / 2016 as well as for SharePoint Online in Office 365.

Let’s imagine a situation where during a day people work with documents in SharePoint Document library. To work with some document user takes it to work and mark it as check out, but at the end of the day, every document should be checked-in back.

Below you can find an example of a small workflow which gets all documents in check-out status and does check-in for each one.

.. image:: /_static/img/check-in-docs-1.png
   :alt:

The action `Get Item by Query <https://plumsail.com/docs/workflow-actions-pack/actions/List%20items%20processing.html#get-items-by-query>`_ was used with the following configuration:

.. image:: /_static/img/check-in-docs-2.png
   :alt:

Notice that the endpoint was “client.svc” to get the data and expand File property to get File/ServerRelativeUrl

To check-in a document `Check-in Document <https://plumsail.com/docs/workflow-actions-pack/actions/Files%20and%20Folders%20processing.html#check-in-document>`_ was used.