Manage credentials for workflow actions on site level
#####################################################

Workflow Actions Pack features an option which will allow you to create more flexible and manageable workflows. This approach is actual only for SharePoint Online in Office 365 version. Workflow Actions Pack for SharePoint 2013 workflows in On-Premises uses account of an user who published a workflow by default.

You can specify default workflow credentials for all workflows on current site or specify credentials for each workflow individually. Those credentials will be used by Workflow Actions Pack actions. Just navigate to ‘Site settings’ and click ‘Workflow Actions Pack’:

.. image:: /_static/img/manage-credentials-3.png
   :alt: 

You will see such dialog:

.. image:: /_static/img/manage-credentials-4.png
   :alt: 

The **Default account** \is an account which will be used to run any workflow action if it is not overridden.

At the picture you can see the list of workflows. Each workflow has **Run account.**  Thus, you can override default account for each workflow by other credentials. Workflow actions from Workflow Actions Pack will use overridden credentials.\

If you want to specify credentials as usual for each workflow action you can do it via properties. AdminLogin and Admin are still available in properties of a workflow action:

.. image:: /_static/img/manage-credentials-5.png
   :alt: 

Is it secure to store credentials at site level?
**************************************************
The credentials are encrypted and saved inside SharePoint. No one can see\original password even if they are administrators. You need to confirm a password each time you configure an account.

.. image:: /_static/img/manage-credentials-6.png
   :alt: 

Do I need to reconfigure all workflows, which I created before?
***************************************************************
No you don’t have to do this. All workflows will work as usual, because each workflow action has already filled AdminLogin and AdminPassword properties, but newly added workflow actions will use the default account. If you have not specified it yet, you need to do it. Just open the link ‘Plumsail Actions Pack’ from ‘Site Administration’ section at the ‘Site settings’:

.. image:: /_static/img/manage-credentials-7.png
   :alt:

How to Upgrade?
***************
To upgrade the Workflow Actions Pack please download the last version and follow the upgrade instruction.

After upgrade please don’t forget open the settings page and set default credentials.