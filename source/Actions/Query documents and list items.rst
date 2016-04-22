Query documents and list items
==================================================


Get Items by Query
--------------------------------------------------
Execute CAML query and get Dictionary with items

Parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  ListId
       -  List for querying
       -  
    *  -  CAML Query
       -  CAML query that will be run
       -  
 
   
     
       
         
        0
       
     
   
                  
                	
    *  -  Items
       -  Output variable for save result
       -  Variable:Items
    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  
                    https://contoso/SiteUrl[%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  RunAsPublisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/GetItems.png
   :alt: Run CAML query and get items SharePoint Online

Copy Document from Library
--------------------------------------------------
Copies the document from the document library to the specified URL. You can copy the document to another document library cross-site or to another folder.

Parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  SourceUrl
       -  The URL of the document to be copied. You can use full URL as well as domain relative URL. We would recommend to use constants from the workflow context.
       -  
                    https://contoso/SiteUrl/LibraryName/FolderName/DocumentName.docx/SiteUrl/LibraryName/FolderName/FileName.docx[%Workflow Context:Current Site URL%]SiteUrl/LibraryName/DocumentName.docx[%Workflow Context:Current Item URL%]
    *  -  DestinationUrl
       -  The URL where the source document will be copied. You can use full URL as well as domain relative URL. We would recommend to use constants from the workflow context.
       -  
                    https://contoso/SiteUrl/LibraryName/FolderName/DocumentName.docx/SiteUrl/LibraryName/FolderName/FileName.docx[%Workflow Context:Current Site URL%]SiteUrl/LibraryName/DocumentName.docx[%Workflow Context:Current Item URL%]
                
    *  -  CopyPermissions
       -  Reserved for future use
       -  
    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  
                    https://contoso/SiteUrl[%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  RunAsPublisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/CopyFile.png
   :alt: Copy file from one library to another SharePoint Online

Move Document from Library
--------------------------------------------------
Moves the document from the document library to the specified URL. You can move the document to another document library cross-site or to another folder.

Parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  SourceUrl
       -  The URL of the document to be moved. You can use full URL as well as domain relative URL. We would recommend to use constants from the workflow context.
       -  
                    https://contoso/SiteUrl/LibraryName/FolderName/DocumentName.docx/SiteUrl/LibraryName/FolderName/FileName.docx[%Workflow Context:Current Site URL%]SiteUrl/LibraryName/DocumentName.docx[%Workflow Context:Current Item URL%]
    *  -  DestinationUrl
       -  The URL where the source document will be moved. You can use full URL as well as domain relative URL. We would recommend to use constants from the workflow context.
       -  
                    https://contoso/SiteUrl/LibraryName/FolderName/DocumentName.docx/SiteUrl/LibraryName/FolderName/FileName.docx[%Workflow Context:Current Site URL%]SiteUrl/LibraryName/DocumentName.docx[%Workflow Context:Current Item URL%]
                
    *  -  CopyPermissions
       -  Reserved for future use
       -  
    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  
                    https://contoso/SiteUrl[%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  RunAsPublisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/MoveFile.png
   :alt: Move file to another document library SharePoint Online

Create Folder
--------------------------------------------------
Create new folder in specific path

Parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  TargetListUrl
       -  The URL of library where need to create a folder. You can use full URL as well as domain relative URL. We would recommend to use constants from the workflow context.
       -  
                    https://contoso/SiteUrl/LibraryName/SiteUrl/LibraryName[%Workflow Context:Current Site URL%]SiteUrl/LibraryName
    *  -  TargetPath
       -  Path that need to create. Action will create all folders that includes to path.
       -  Projects/Project1 Documents/2014 June
    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  
                    https://contoso/SiteUrl[%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  RunAsPublisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/CreateFolder.png
   :alt: Create folder in document library SharePoint Online

Remove Folder
--------------------------------------------------
Remove specific folder

Parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  TargetListUrl
       -  The URL of library where the source folder will be copied. You can use full URL as well as domain relative URL. We would recommend to use constants from the workflow context.
       -  
                    https://contoso/SiteUrl/LibraryName/SiteUrl/LibraryName[%Workflow Context:Current Site URL%]SiteUrl/LibraryName
    *  -  TargetPath
       -  Inner path in document library, where folder will be deleted
       -  Documents/Projects/Project1Folder1/SubFolder
    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  
                    https://contoso/SiteUrl[%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  RunAsPublisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/RemoveFolder.png
   :alt: Remove specific folder SharePoint Online

Copy Folder from Library
--------------------------------------------------
Copies the folder from the document library to the specified URL. You can copy the folder to another document library cross-site or to another folder.

Parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  SourceUrl
       -  The URL of the folder to be copied. You can use full URL as well as domain relative URL. We would recommend to use constants from the workflow context.
       -  
                    https://contoso/SiteUrl/LibraryName/FolderName//SiteUrl/LibraryName/FolderName[%Workflow Context:Current Site URL%]SiteUrl/LibraryName
    *  -  TargetListUrl
       -  The URL of library where the source folder will be copied. You can use full URL as well as domain relative URL. We would recommend to use constants from the workflow context.
       -  
                    https://contoso/SiteUrl/LibraryName/SiteUrl/LibraryName[%Workflow Context:Current Site URL%]SiteUrl/LibraryName
    *  -  TargetPath
       -  Inner path in document library, where files will be copied
       -  Documents/Projects/Project1Folder1/SubFolder
    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  
                    https://contoso/SiteUrl[%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  RunAsPublisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/MoveAttachments.png
   :alt: Copy folder from one library to another SharePoint Online

Move Folder from Library
--------------------------------------------------
Moves the folder from the document library to the specified URL. You can move the folder to another document library cross-site or to another folder.

Parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  SourceUrl
       -  The URL of the folder to be copied. You can use full URL as well as domain relative URL. We would recommend to use constants from the workflow context.
       -  
                    https://contoso/SiteUrl/LibraryName/FolderName//SiteUrl/LibraryName/FolderName[%Workflow Context:Current Site URL%]SiteUrl/LibraryName
    *  -  TargetListUrl
       -  The URL of library where the source folder will be copied. You can use full URL as well as domain relative URL. We would recommend to use constants from the workflow context.
       -  
                    https://contoso/SiteUrl/LibraryName/SiteUrl/LibraryName[%Workflow Context:Current Site URL%]SiteUrl/LibraryName
    *  -  TargetPath
       -  Inner path in document library, where files will be copied
       -  Documents/Projects/Project1Folder1/SubFolder
    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  
                    https://contoso/SiteUrl[%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  RunAsPublisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/MoveFolder.png
   :alt: Move folder to another document library SharePoint Online

Copy Attachments to URL
--------------------------------------------------
Copy attachments from the list item to the library

Parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  ListUrl
       -  The URL of the source list. You can use full URL as well as domain relative URL. We would recommend to use constants from the workflow context.
       -  https://contoso/SiteUrl/Lists/Issues[%Workflow Context:Current Site URL%]SiteUrl/Lists/Issues
    *  -  ItemId
       -  ID of the source item
       -  22Variable:ItemId
    *  -  DestinationUrl
       -  The URL of folder where the source documents will be copied
       -  https://contoso/SiteUrl/LibraryName/FolderName//SiteUrl/LibraryName/FolderName/[%Workflow Context:Current Site URL%]SiteUrl/LibraryName/
    *  -  CopyPermissions
       -  Reserved for future use
       -  
    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  
                    https://contoso/SiteUrl[%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  RunAsPublisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/CopyAttachments.png
   :alt: Copy attachments SharePoint Online

Move Attachments to URL
--------------------------------------------------
Move attachments from the list item to the library

Parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  ListUrl
       -  The URL of the source list. You can use full URL as well as domain relative URL. We would recommend to use constants from the workflow context.
       -  https://contoso/SiteUrl/Lists/Issues[%Workflow Context:Current Site URL%]SiteUrl/Lists/Issues
    *  -  ItemId
       -  ID of the source item
       -  22Variable:ItemId
    *  -  DestinationUrl
       -  The URL of folder where the source documents will be moved
       -  https://contoso/SiteUrl/LibraryName/FolderName//SiteUrl/LibraryName/FolderName/[%Workflow Context:Current Site URL%]SiteUrl/LibraryName/
    *  -  CopyPermissions
       -  Reserved for future use
       -  
    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  
                    https://contoso/SiteUrl[%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  RunAsPublisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/MoveAttachments.png
   :alt: Move attachments to document library SharePoint Online

Get Attachments to Dictionary
--------------------------------------------------
Get list of attachments from list item to Dictionary

Parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  ListUrl
       -  The URL of the source list. You can use full URL as well as domain relative URL. We would recommend to use constants from the workflow context.
       -  https://contoso/SiteUrl/Lists/Issues[%Workflow Context:Current Site URL%]SiteUrl/Lists/Issues
    *  -  ItemId
       -  ID of the source item
       -  22Variable:ItemId
    *  -  Items
       -  Output variable for save result
       -  Variable:Items
    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  
                    https://contoso/SiteUrl[%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  RunAsPublisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/GetAttachments.png
   :alt: Get attachments to dictionary SharePoint Online

