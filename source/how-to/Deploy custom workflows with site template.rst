Deploy custom workflows with site template
##########################################

It is common scenario when you did some customizations, saved site as template and want to reuse it in SharePoint 2013 or in SharePoint Online (Office 365). Such site templates can include workflows with custom workflow actions. Unfortunately if you save site with custom workflow actions as template and then try to create new site you can receive such annoying error:

.. error::

    Microsoft.Workflow.Client.ActivityNotFoundException:Theactivity named'WorkflowXaml_988fe3c3_dc3e_47a9_8ff3_c912c82eb56d'fromscope'/spo/216722f1-1dc0-4c6d-aafd-86b12ef60a14/1f87e1ae-da77-44d4-92d1-502507b5f2d4/34ceaf02-5217-46be-a307-e09dd93da230'wasnotfound.HTTP headers receivedfromthe server-ActivityId:224e672a-4e00-44ed-8b55-894a059608c2.NodeId:.Scope:.ClientActivityId:f6cadd9c-c011-1000-aa42-85eedd28fc19.---\>System.Net.WebException:Theremote server returned an error

The reason of such behavior is related to incorrect processing of template by SharePoint 2013.

That's why it was implemented such utility because some of our customers had questions about correct site template provisioning. Especially when custom site template included workflow actions from our product `Workflow Actions Pack </workflow-actions-pack/>`_ .\

Use case – deploy a new web with configured workflows
*****************************************************
Save Site as Template
---------------------
The first step, you need to create a Site template. To do this navigate to Site Settings -\>Save site as Template (In Site Actions section). If you don’t see this link you can navigate using\direct link. For example:https://yourSiteUrl/sites/WebUrl **/_layouts/15/savetmpl.aspx** 

.. image:: /_static/img/deploy-custom-workflows-1.png
   :alt: 

Then fill all the fields and check the checkbox “Include content” (If you don’t do this\the workflows won’t be included into template).

.. image:: /_static/img/deploy-custom-workflows-2.png
   :alt: 

When the operation will be completed, please download the WSP package from the solution gallery.

.. image:: /_static/img/deploy-custom-workflows-3.png
   :alt: 

Click on the template to download it:
.. image:: /_static/img/deploy-custom-workflows-4.png

Patch the site template
-----------------------
As described earlier if we try to create a new site we can get the following error:

.. error::

    Microsoft.Workflow.Client.ActivityNotFoundException:Theactivity named'WorkflowXaml_988fe3c3_dc3e_47a9_8ff3_c912c82eb56d'fromscope'/spo/216722f1-1dc0-4c6d-aafd-86b12ef60a14/1f87e1ae-da77-44d4-92d1-502507b5f2d4/34ceaf02-5217-46be-a307-e09dd93da230'wasnotfound.HTTP headers receivedfromthe server-ActivityId:224e672a-4e00-44ed-8b55-894a059608c2.NodeId:.Scope:.ClientActivityId:f6cadd9c-c011-1000-aa42-85eedd28fc19.---\>System.Net.WebException:Theremote server returned an error

To avoid the error we have to patch the WSP package with help of a small utility `TemplatePackageFix <https://github.com/RFlipper/TemplatePackageFix/releases>`_ . I described it in detail in my `previous article </blog/2015/01/deploy-sharepoint-2013-workflow-via-site-template/>`_ . This utility simply moves all workflows to separate feature. Thus, site will be created by template without workflows and then you will be able to activate the feature to deploy workflows.

You can download it from `the following link <https://github.com/RFlipper/TemplatePackageFix/releases>`_ . Please download it and extract to any directory.

To run, press “Win + R” and run the CMD.\

.. image:: /_static/img/deploy-custom-workflows-5.png
   :alt: 

Next step is to specify path to the program and path to the WSP package which we downloaded.\The command can look like this:



c:\YourFolder\TempatePackageFix.exe 

After a few seconds you will see “fixed” message:

.. image:: /_static/img/deploy-custom-workflows-6.png
   :alt: 

That is all. Your WSP package has been patched, all workflows have been\moved to another feature.The last step is to upload the WSP package to the solution gallery.

Create new Site based on saved template
---------------------------------------
Now you can upload patched wps package with site template to your solution gallery and activate it. Then,\you can create a new site. To do this\this navigate to “Site Contents”.

.. image:: /_static/img/deploy-custom-workflows-7.png
   :alt: 

\

Then,\scroll down and press “new subsite”:

.. image:: /_static/img/deploy-custom-workflows-8.png
   :alt: 

Please fill all the fields and select your site template on “Custom” tab. Note, if you can’t find your site template, most likely you selected incorrect language.

.. image:: /_static/img/deploy-custom-workflows-9.png
   :alt: 

The last step before you can use the site, you need to activate the “Workflow Actions Pack” feature (This will make available custom workflow actions) and “Template workflows” feature (it contains all your workflows).

.. image:: /_static/img/deploy-custom-workflows-10.png
   :alt: 

