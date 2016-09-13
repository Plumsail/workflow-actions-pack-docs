Installation for SharePoint 2013 / 2016
==================================================

Install
--------------------------------------------------

Before installing Workflow Actions Pack ensure that Workflow Manager is configured for your farm. Workflow Manager allows to create and execute SharePoint 2013 workflows. See `Workflow Manager configuration guide <http://technet.microsoft.com/en-us/library/jj658588(v=office.15).aspx>`_.


`Download setup file </workflow-actions-pack/download/>`_ and run it on one of the servers in your SharePoint 2013 farm as Farm Administrator. Follow the wizard steps.


After that you have to activate Web Application level feature **Plumsail Auth Service** for this please open your central administration site and navigate to **Application Management** section, click on the link **Manage web application**, choose your using web application, click to the **Features** button on the ribbon and activate the **Plumsail Auth Service** feature.
    
.. image:: /_static/img/SiteAdm_appMng_MngWebApp.png
   :alt: SharePoint Application Management

Next, you have to activate feature on your site. Navigate to the site, open site settings and select Manage site features.

.. image:: /_static/img/WFPack_6.-ManageSiteFeatures.png
   :alt: SharePoint Manage Site features

Find feature called **Plumsail Workflow Actions Pack** and click **Activate**

.. image:: /_static/img/WFPack_7.ActivateFeature.png
   :alt: SharePoint Activate Feature

Now, you can find the following actions in SharePoint Designer under Plumsail section

.. image:: /_static/img/WFPack_8.CheckInSPD.png
   :alt: SharePoint Designer new Actions

Install license
--------------------------------------------------

* Buy **Workflow Action Pack for SharePoint 2013** license for each web front-end server.
* Download Hardware ID Generator. You can find download link in the e-mail message with order number from our online store. Run it on all WFE-servers of your farm. Copy generated keys and send them to `sales@plumsail.com <sales@plumsail.com>`_ with your order number in the subject.
* We will generate licenses for you and will send them to your e-mail within one day.
* Place received .license files in the root folder of all SharePoint web-applications on WFE-servers according to generated keys. 
	If you use port 80 it is usually here: ``c:\inetpub\wwwroot\wss\VirtualDirectories\80\``


Uninstall
--------------------------------------------------

Run setup file and choose **Remove**, then finish the installation wizard.

.. image:: /_static/img/RemoveWFActivityPack.png
   :alt: RemoveWFActivityPack


Upgrade
--------------------------------------------------

Firstly, you have to deactivate **Plumsail Workflow Actions Pack** feature at the site level.
`Download setup file </workflow-actions-pack/download/>`_ and run it on one of the servers in your Sharepoint 2013 farm as Farm Administrator. Choose **Upgrade** and follow the wizard steps.

.. image:: /_static/img/UpgradeWFActivityPack.png
   :alt: Upgrade workflow actions pack

Find the feature called **Plumsail Workflow Actions** Pack and click **Activate**

.. image:: /_static/img/WFPack_7.ActivateFeature.png
   :alt: SharePoint Activate Feature



Upgrade workflows
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Sometimes after upgrade WSP package, you also need to upgrade your workflows. 
To upgrade workflows you need to navigate to Site Settings -> Plumsail Workflow Actions and click ‘Upgrade’ button for workflows where you see it. After upgrading of workflows you need to clear Sharepoint Designer cache and open it again. You may need to reopen SharePoint Designer second time, it is specific of SharePoint Designer.

.. image:: /_static/img/WFPack_Upgrade1.png
   :alt: SharePoint upgrade workflows step 1


Known Issues
--------------------------------------------------

SharePoint Designer issues
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

SharePoint Designer stores cached workflow actions, that is why after solution upgrade you may need to perform few actions.
You need to clear SharePoint Designer 2013 cache, otherwise it can show you the error message because it uses old cached version of workflow actions. To clear cache you need to execute following command from the command line as administrator on your PC and reopen SharePoint Designer:

::

   rmdir "%LOCALAPPDATA%\Microsoft\WebsiteCache\" /s /q
   rmdir "%APPDATA%\Microsoft\SharePoint Designer\ProxyAssemblyCache\" /s /q

Or you can `download and execute the bat file </wp-content/uploads/Files/WFActionsPack/ClearSPDesignerCache.bat>`_.

After clearing the cache and running SharePoint Designer you may need to close and open SharePoint Designer one more time, then the error should disappear.
We also recommend to install recent updates for SharePoint Designer 2013. This will help to avoid annoying error when configuring workflows.

If you use SharePoint Designer on the same server where has installed Workflow Manager and see the message **Server-side activities have been updated**, please check `the link <http://www.jrjlee.com/2014/10/server-side-activities-have-been-updated.html>`_.

We also recommend to install `recent updates for SharePoint Designer 2013 </workflow-actions-pack/docs/recommended-sharepoint-designer-updates/>`_. This will help to avoid annoying error when configuring workflows.
