What is SharePoint Web Front End server (WFE)
=============================================

A server which handles web page requests from users is called Web Front End (WFE). 
Thus, each time when user opens a SharePoint page in a browser, it is processed by WFE server. 
SharePoint farm may have multiple such servers. If there are multiple WFE servers, Network Load Balancer is distributing requests between them. 
It is the way to scale SharePoint.


Many Plumsail products are licensed per Web Front End server. 
You may need to calculate number of WFE servers in your SharePoint farm to purchase correct number of licenses.


SharePoint WFE server usually has “Microsoft SharePoint Foundation Web Application” service started. 
You can check it in SharePoint Central Administration: :code:`Central Administration > System Settings > Manage services on server.`  
In the :code:`Services on server` page, select server and check if the service is started. 
If it’s started, the selected server is acting as a web front-end server.


.. image:: /../_static/img/SP_Foundation_WebApp_Service_zps1dcff207.png
    :alt: WFE


Thus, you can switch between your servers and find all Web Front End servers.


