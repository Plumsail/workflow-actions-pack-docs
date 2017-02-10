Documents and folders processing
==================================================


Copy Document from Library
--------------------------------------------------
Copies the document from the document library to the specified URL. You can copy the document to another document library cross-site or to another folder.

Output Parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  File ID
       -  The ID of the copied file
       -  ``1024``
    *  -  File Url
       -  The URL of the copied file
       -  ``https://contoso.sharepoint.com/Shared Documents/Example.docx``

Input Parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  SourceUrl
       -  The URL of the document to be copied. You can use full URL as well as domain relative URL. We would recommend to use constants from the workflow context.
       -  ::

            https://contoso/SiteUrl/LibraryName/FolderName/DocumentName.docx
            /SiteUrl/LibraryName/FolderName/FileName.docx 
            [%Workflow Context:Current Site URL%]SiteUrl/LibraryName/DocumentName.docx 
            [%Workflow Context:Current Item URL%]

    *  -  DestinationUrl
       -  The URL where the source document will be copied. You can use full URL as well as domain relative URL. We would recommend to use constants from the workflow context.
       -  ::

            https://contoso/SiteUrl/LibraryName/FolderName/DocumentName.docx
            /SiteUrl/LibraryName/FolderName/FileName.docx
            [%Workflow Context:Current Site URL%]SiteUrl/LibraryName/DocumentName.docx
            [%Workflow Context:Current Item URL%]

    *  -  Keep Source Link
       -  Keep document as linked
       -  `False`
    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  ::

            https://contoso/SiteUrl
            [%Workflow Context:Current Site URL%]subSite

    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  RunAsPublisher
       -  Detects whether the workflow action has to be runned under the user account who published the workflow (for SharePoint 2013 on-premise only).
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/CopyFile.png
   :alt: Copy file from one library to another SharePoint Online

Move Document from Library
--------------------------------------------------
Moves the document from the document library to the specified URL. You can move the document to another document library cross-site or to another folder.

Output Parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  File ID
       -  The ID of the moved file
       -  ``1024``
    *  -  File Url
       -  The URL of the moved file
       -  ``https://contoso.sharepoint.com/Shared Documents/Example.docx``

Input Parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  SourceUrl
       -  The URL of the document to be moved. You can use full URL as well as domain relative URL. We would recommend to use constants from the workflow context.
       -  ::

            https://contoso/SiteUrl/LibraryName/FolderName/DocumentName.docx
            /SiteUrl/LibraryName/FolderName/FileName.docx 
            [%Workflow Context:Current Site URL%]SiteUrl/LibraryName/DocumentName.docx 
            [%Workflow Context:Current Item URL%]

    *  -  DestinationUrl
       -  The URL where the source document will be moved. You can use full URL as well as domain relative URL. We would recommend to use constants from the workflow context.
       -  ::

            https://contoso/SiteUrl/LibraryName/FolderName/DocumentName.docx
            /SiteUrl/LibraryName/FolderName/FileName.docx
            [%Workflow Context:Current Site URL%]SiteUrl/LibraryName/DocumentName.docx
            [%Workflow Context:Current Item URL%]

    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  ::

            https://contoso/SiteUrl
            [%Workflow Context:Current Site URL%]subSite

    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  RunAsPublisher
       -  Detects whether the workflow action has to be runned under the user account who published the workflow (for SharePoint 2013 on-premise only).
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/MoveFile.png
   :alt: Move file to another document library SharePoint Online

Remove Document by URL
--------------------------------------------------
Remove the document by a specific URL 

Input Parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  SourceUrl
       -  The URL of the document to be removed. You can use full URL as well as domain relative URL. We would recommend to use constants from the workflow context.
       -  ::

            https://contoso/SiteUrl/LibraryName/FolderName/DocumentName.docx
            /SiteUrl/LibraryName/FolderName/FileName.docx 
            [%Workflow Context:Current Site URL%]SiteUrl/LibraryName/DocumentName.docx 
            [%Workflow Context:Current Item URL%]

    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  ::

            https://contoso/SiteUrl
            [%Workflow Context:Current Site URL%]subSite

    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  RunAsPublisher
       -  Detects whether the workflow action has to be runned under the user account who published the workflow (for SharePoint 2013 on-premise only).
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/RemoveFile.png
   :alt: Remove file by a URL

Copy DocumentSet
--------------------------------------------------
It copies the document set from the document library to the specified URL. You can copy the document sets to another document library cross-site or to another folder.

Output Parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  DocSet ID
       -  The ID of the moved Document Set
       -  ``1025``
    *  -  DocSet Url 
       -  The URL of the moved Document Set
       -  ``https://contoso.sharepoint.com/Shared Documents/Example``


Input Parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  SourceUrl
       -  The URL of the document set to be copied. You can use full URL as well as domain relative URL. We would recommend to use constants from the workflow context.
       -  ::

            https://contoso/SiteUrl/LibraryName/DocSetName
            /SiteUrl/LibraryName/FolderName/DocSetName
            [%Workflow Context:Current Site URL%]SiteUrl/LibraryName/DocumentSetName
            [%Workflow Context:Current Item URL%]

    *  -  DestinationUrl
       -  The URL where the source document set will be copied. You can use full URL as well as domain relative URL. We would recommend to use constants from the workflow context.
          ``If the url ends with slash '/' the document sets will be placed in this folder without name changes. Otherwise the Document set will be renamed.``

       -  ::

            https://contoso/SiteUrl/LibraryName/FolderName/
            /SiteUrl/LibraryName/FolderName/
            [%Workflow Context:Current Site URL%]SiteUrl/LibraryName/DocSetName

    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  ::

            https://contoso/SiteUrl
            [%Workflow Context:Current Site URL%]subSite

    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  RunAsPublisher
       -  Detects whether the workflow action has to be runned under the user account who published the workflow (for SharePoint 2013 on-premise only).
       -  Yes

Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/CopyDocSetTo.png
   :alt: Copy document set from one library to another in SharePoint Online

Move DocumentSet
--------------------------------------------------
It moves the document set from the document library to the specified URL. You can move the document sets to another document library cross-site or to another folder.

Output Parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  DocSet ID
       -  The ID of the moved Document Set
       -  ``1025``
    *  -  DocSet Url 
       -  The URL of the moved Document Set
       -  ``https://contoso.sharepoint.com/Shared Documents/Example``


Input Parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  SourceUrl
       -  The URL of the document set to be copied. You can use full URL as well as domain relative URL. We would recommend to use constants from the workflow context.
       -  ::

            https://contoso/SiteUrl/LibraryName/DocSetName
            /SiteUrl/LibraryName/FolderName/DocSetName
            [%Workflow Context:Current Site URL%]SiteUrl/LibraryName/DocumentSetName
            [%Workflow Context:Current Item URL%]

    *  -  DestinationUrl
       -  The URL where the source document set will be copied. You can use full URL as well as domain relative URL. We would recommend to use constants from the workflow context.
          ``If the url ends with slash '/' the document sets will be placed in this folder without name changes. Otherwise the Document set will be renamed.``

       -  ::

            https://contoso/SiteUrl/LibraryName/FolderName/
            /SiteUrl/LibraryName/FolderName/
            [%Workflow Context:Current Site URL%]SiteUrl/LibraryName/DocSetName

    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  ::

            https://contoso/SiteUrl
            [%Workflow Context:Current Site URL%]subSite

    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  RunAsPublisher
       -  Detects whether the workflow action has to be runned under the user account who published the workflow (for SharePoint 2013 on-premise only).
       -  Yes

Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/CopyDocSetTo.png
   :alt: Copy document set from one library to another in SharePoint Online


Create Folder by URL
--------------------------------------------------
Creates a new folder in the document library by the specified path

Output Parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  Folder ID
       -  The ID of the created folder
       -  ``1026``


Input Parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  Folder Url
       -  The Url of the folder. If you specify full path, you can create several folders.
       -  ::

            https://contoso/SiteUrl/LibraryName/SiteUrl/LibraryName1/SubLib2
            [%Workflow Context:Current Site URL%]SiteUrl/LibraryName

    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  ::

            https://contoso/SiteUrl
            [%Workflow Context:Current Site URL%]subSite

    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  RunAsPublisher
       -  Detects whether the workflow action has to be runned under the user account who published the workflow (for SharePoint 2013 on-premise only).
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/CreateFolder.png
   :alt: Create folder in document library SharePoint Online

Create Folder in list
--------------------------------------------------
Creates a new folder in the document library or list using the specified path.

Input Parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  Target List Url
       -  The URL of the library of list where the folder will be created. You can use full URL as well as domain relative URL. We would recommend to use constants from the workflow context.
       -  ::

            https://contoso/SiteUrl/LibraryName/SiteUrl/LibraryName
            [%Workflow Context:Current Site URL%]SiteUrl/LibraryName

    *  -  TargetPath
       -  The path where the folder will be created. The workflow action will create all folders included into the path.
       -  ``Projects/Project1Documents/2014 June``
    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  ::

            https://contoso/SiteUrl
            [%Workflow Context:Current Site URL%]subSite

    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  RunAsPublisher
       -  Detects whether the workflow action has to be runned under the user account who published the workflow (for SharePoint 2013 on-premise only).
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/CreateFolder.png
   :alt: Create folder in document library SharePoint Online

Remove Folder by Url
--------------------------------------------------
Removes the folder from the document library or list by the specified Url

Input Parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  Folder Url
       -  The URL of the library where the source folder will be removed. You can use full URL as well as domain relative URL. We would recommend to use constants from the workflow context.
       -  ::

            https://contoso/SiteUrl/LibraryName/SiteUrl/LibraryName
            [%Workflow Context:Current Site URL%]SiteUrl/LibraryName

    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  ::

            https://contoso/SiteUrl
            [%Workflow Context:Current Site URL%]subSite

    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  RunAsPublisher
       -  Detects whether the workflow action has to be runned under the user account who published the workflow (for SharePoint 2013 on-premise only).
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/RemoveFolderByUrl.png 
   :alt: Remove specific folder SharePoint Online

Copy Folder from Library
--------------------------------------------------
Copies the folder from the document library to the specified URL. You can copy the folder to another document library cross-site or to another folder.

Output Parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  Folder ID
       -  The ID of the moved Document Set
       -  ``1030``
    *  -  Folder Url 
       -  The URL of the moved Document Set
       -  ``https://contoso.sharepoint.com/Shared Documents/Example``

Input Input Parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  Source folder url
       -  The URL of the folder to be copied. You can use full URL as well as domain relative URL. We would recommend to use constants from the workflow context.
       -  ::

            https://contoso/SiteUrl/LibraryName/FolderName/
            /SiteUrl/LibraryName/FolderName
            [%Workflow Context:Current Site URL%]SiteUrl/LibraryName

    *  -  Destination folder url
       -  The URL of the library where the source folder will be copied. You can use full URL as well as domain relative URL. We would recommend to use constants from the workflow context.
       -  ::

            https://contoso/SiteUrl/LibraryName/SiteUrl/LibraryName/Folder1
            [%Workflow Context:Current Site URL%]SiteUrl/LibraryName/

    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  ::

            https://contoso/SiteUrl
            [%Workflow Context:Current Site URL%]subSite

    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  RunAsPublisher
       -  Detects whether the workflow action has to be runned under the user account who published the workflow (for SharePoint 2013 on-premise only).
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/CopyFolderFromLib.png 
   :alt: Copy folder from one library to another SharePoint Online

Move Folder from Library
--------------------------------------------------
Moves the folder from the document library to the specified URL. You can move the folder to another document library cross-site or to another folder.

Output Parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  Folder ID
       -  The ID of the moved Document Set
       -  ``1030``
    *  -  Folder Url 
       -  The URL of the moved Document Set
       -  ``https://contoso.sharepoint.com/Shared Documents/Example``

Input Parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  Source folder url
       -  The URL of the folder to be copied. You can use full URL as well as domain relative URL. We would recommend to use constants from the workflow context.
       -  ::

            https://contoso/SiteUrl/LibraryName/FolderName/
            /SiteUrl/LibraryName/FolderName
            [%Workflow Context:Current Site URL%]SiteUrl/LibraryName

    *  -  Destination folder Url
       -  The URL of the library where the source folder will be copied. You can use full URL as well as domain relative URL. We would recommend to use constants from the workflow context.
       -  ::

            https://contoso/SiteUrl/LibraryName/SiteUrl/LibraryName
            [%Workflow Context:Current Site URL%]SiteUrl/LibraryName/

    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  ::

            https://contoso/SiteUrl
            [%Workflow Context:Current Site URL%]subSite

    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  RunAsPublisher
       -  Detects whether the workflow action has to be runned under the user account who published the workflow (for SharePoint 2013 on-premise only).
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/MoveFolderFromUrl.png 
   :alt: Move folder to another document library SharePoint Online

