Use Call SharePoint REST Service instead of standard Call HTTP Web Service
##########################################################################

You are probably familiar that using SharePoint Designer you can consume SharePoint REST API.

The API is very flexible and allows you to manipulate items, lists and almost every aspect of SharePoint. On the Internet, you can find many articles describing how to use it and how to correctly configure the workflow.

In most cases this will be very simple use cases, it's supposed that this is because the complexity of the workflow increasing dramatically with number or required requests and processing data.

We are in Plumsail try to simplify things, that is why we added “ `Get Items by Query </docs/workflow-actions-pack/actions/List%20items%20processing.html#get-items-by-caml-query>`_ ” workflow action.

Let’s have a look at the following article: `Call HTTP Web Service Using SharePoint Designer 2013 (SPD) <http://www.c-sharpcorner.com/UploadFile/58e23e/call-http-web-service-using-sharepoint-designer-2013-spd/>`_

A guy describes how to create a simple workflow which gets items from a list and log a Title of each item to the history list.

I reproduced the case and it takes almost half an hour to create it.


.. image:: /_static/img/rest-oob-vs-plumsail-1.png
   :alt: Get Items via REST Service out of the box 

\
 
.. image:: /_static/img/rest-oob-vs-plumsail-2.png
   :alt: 

\

.. image:: /_static/img/rest-oob-vs-plumsail-3.png
   :alt: 

\

.. image:: /_static/img/rest-oob-vs-plumsail-4.png
   :alt: 

After that, it was installed `Workflow Actions Pack <https://plumsail.com/workflow-actions-pack/>`_ and it was created the same use case\but using actions from Workflow Actions Pack. Of course, it took just 5 mins and the final workflow looks more clear for anyone who has to maintain it in the future.


.. image:: /_static/img/rest-oob-vs-plumsail-5.png
   :alt: Get Items via REST API SharePoint Workflow


Now let’s imagine that you need to implement more complex workflow, indeed in a production environment, it was saw workflows which take 3-5 pages and it’s hard to understand their logic and it's not mentioned that consultant that creates it costs a lot of money.\Using Actions Pack you can save your time and your money. Moreover, `Workflow Actions Pack <https://plumsail.com/workflow-actions-pack/>`_ \allows you to get data from another site or even tenant, it opens new possibilities comparing with OOB workflows.\