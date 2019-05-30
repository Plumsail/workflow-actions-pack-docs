Use different Get items actions to query lists
##############################################

This article will explain how get items workflow actions work and how to use them to query list items from SharePoint 2013 / 2016 list. Those actions can be used to query list items cross-site as well as in current site. This approach works in SharePoint 2013 / 2016 / 2019 as well as for SharePoint Online in Office 365.

We have the following actions that you can use to get items from a list:

* `Get Items by Query <https://plumsail.com/docs/workflow-actions-pack/actions/List%20items%20processing.html#get-items-by-query>`_
* `Get Items from View <https://plumsail.com/docs/workflow-actions-pack/actions/List%20items%20processing.html#get-items-from-view>`_
* `Get Items by CAML Query <https://plumsail.com/docs/workflow-actions-pack/actions/List%20items%20processing.html#get-items-by-caml-query>`_
* `Get Items by CAML Query (Many Lists) <https://plumsail.com/docs/workflow-actions-pack/actions/List%20items%20processing.html#get-items-by-caml-query-many-lists>`_

They all starts from “Get Items” but they have some nuances of usage and actually could be useful for different situations.

Get Items by Query
------------------

This is the most modern and preferable implementation of get items action. We recommend it for using. Inside, it is based on REST query to “listdata.svc” or “client.svc” web services. By default, it uses listdata.svc because it allows a lot more operators like startswith, substringof, top skip and others. You can find some useful examples in the following article: `SharePoint: Adventures with the REST API Part 1 <https://platinumdogs.me/2013/03/14/sharepoint-adventures-with-the-rest-api-part-1/>`_. However, you can change service endpoint to client.svc, for some cases it could be more convenient and maybe a bit more familiar because when you use such implementation the request goes through “_api/web/lists” endpoint. So many people are knowing how to work with this REST API and on the Internet, there is a lot of articles and documentation how to work with this service.

To know more about OData queries, I would recommend check out the following article:

`Use OData query operations in SharePoint REST requests <https://msdn.microsoft.com/en-us/library/office/fp142385.aspx>`_

`Understanding SharePoint’s REST and Search API Part 1 – Selecting Items <http://michaelsoriano.com/understanding-sharepoint-rest-api-part-1-selecting-items/>`_

Some additional links:

`Limitations of SharePoint ListData.svc <https://allthatjs.com/2012/07/20/limitations-of-sharepoint-listdata-svc/>`_

 
Get Items from View
-------------------

I suppose this is the most user-friendly action because everything you need to do it is just to configure a view for a list via SharePoint UI and specify the name of the view as a parameter. After that, you will get list items. You don’t need to know REST or CAML, you can configure everything via UI.

 
Get Items by CAML Query
-----------------------

This workflow action designed for true SharePoint developers, you can create a query manually and there are no any limitations. Currently, it used rarely, but you should know about this if you want to implement some complex scenario and of course you should be familiar with CAML queries.

 
Get Items by CAML Query (Many Lists)
------------------------------------

Some old developers maybe know about SPSiteDataQuery object that was available in SSOM only. And this workflow action is an almost full analog of this object. You can query many lists at once using the same CAML query. Personally, I would not recommend to use it because in most cases you can find a simpler workaround.