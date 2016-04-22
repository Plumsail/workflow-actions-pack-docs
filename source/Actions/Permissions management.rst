Permissions management
==================================================


Add User to SharePoint Group
--------------------------------------------------
Add user to a specific group

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  User
       -  Login, email or display name of user which will be added to a specific group. Also you can specify multiple items using semicolon ';' delimited
       -  Jack Jonson
    *  -  Group
       -  Name or ID of group
       -  Approvers
    *  -  AdminEmail
       -  E-mail of the SharePoint administrator (for Office 365 only).
       -  admin@contoso.com
    *  -  AdminPassword
       -  Password of the SharePoint administrator (for Office 365 only).
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  https://contoso/SiteUrl
            [%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  Run as account of publisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/AddUserToGroup.png
   :alt: Add User to SharePoint Group

Remove User from SharePoint Group
--------------------------------------------------
Remove an user from a specific group

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  User
       -  Login, email or display name of user which will be added to a specific group. Also you can specify multiple items using semicolon ';' delimited
       -  Jack Jonson
    *  -  Group
       -  Name or ID of group
       -  Approvers
    *  -  AdminEmail
       -  E-mail of the SharePoint administrator (for Office 365 only).
       -  admin@contoso.com
    *  -  AdminPassword
       -  Password of the SharePoint administrator (for Office 365 only).
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  https://contoso/SiteUrl
          [%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  Run as account of publisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/RemoveUserFromGroup.png
   :alt: Remove User from SharePoint Group

Is User Member of SharePoint Group
--------------------------------------------------
Checking if a user is a member in a SharePoint group

Output parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  Result
       -  Boolean result of checking
       -  True


Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  User
       -  Login, email or display name of user for checking if he is a member in the specified group
       -  Jack Jonson
    *  -  Group
       -  Name or ID of group
       -  Approvers
    *  -  AdminEmail
       -  E-mail of the SharePoint administrator (for Office 365 only).
       -  admin@contoso.com
    *  -  AdminPassword
       -  Password of the SharePoint administrator (for Office 365 only).
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  https://contoso/SiteUrl
          [%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  Run as account of publisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/CheckUserInGroup.png
   :alt: Is User Member of SharePoint Group

Get Members of SharePoint Group
--------------------------------------------------
Get members of SharePoint Group

Output parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  Users
       -  Result is Dynamic value
       -  ::

              [{
                  "Id": "25",
                  "LoginName": "i:0#.f|membership|admin@contoso.onmicrosoft.com",
                  "Email": "admin@contoso.onmicrosoft.com"
              }, {
                  "Id": "32",
                  "LoginName": "i:0#.f|membership|m.anderson@contoso.onmicrosoft.com",
                  "Email": "m.anderson@contoso.onmicrosoft.com"
              }]
                              


Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  Group
       -  Name or ID of group
       -  Approvers
    *  -  AdminEmail
       -  E-mail of the SharePoint administrator (for Office 365 only).
       -  admin@contoso.com
    *  -  AdminPassword
       -  Password of the SharePoint administrator (for Office 365 only).
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  https://contoso/SiteUrl[%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  Run as account of publisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/GetMembersGroup.png
   :alt: Get Members of SharePoint Group

Set Up Default Group for the Site
--------------------------------------------------
You can configure default groups for the site it is analogue of the permsetup.aspx page.

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  Group name
       -  Name or ID of group
       -  Sales owners
    *  -  Group type
       -  type of the group: owners, members or visitors
       -  Owners
    *  -  AdminEmail
       -  E-mail of the SharePoint administrator (for Office 365 only).
       -  admin@contoso.com
    *  -  AdminPassword
       -  Password of the SharePoint administrator (for Office 365 only).
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  https://contoso/SiteUrl
          [%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  Run as account of publisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/ChangeDefaultGroups.png
   :alt: Set Up Groups for the Site

Grant Permission on Site
--------------------------------------------------
Grant specific permissions to an user site

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  Role Type
       -  permission levels:
                   * Full control
                   * Design
                   * Edit
                   * Contribute
                   * Read
                   * ViewOnly
                
       -  5
    *  -  User or group
       -  Login, Email or Name of the User or Group. Also you can specify multiple items using semicolon ';' delimited
       -  Workflow Context:Initiator
    *  -  AdminEmail
       -  E-mail of the SharePoint administrator (for Office 365 only).
       -  admin@contoso.com
    *  -  AdminPassword
       -  Password of the SharePoint administrator (for Office 365 only).
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  https://contoso/SiteUrl[%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  Run as account of publisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/GrantPermissionOnWeb.png
   :alt: Grant Permission on Site

Remove Permissions from Site
--------------------------------------------------
Delete specific permissions from Site for specified user or group

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  Role Type
       -  permission levels:
                   * Full control
                   * Design
                   * Edit
                   * Contribute
                   * Read
                   * ViewOnly
                
       -  5
    *  -  User or group
       -  Login, Email or Name of the User or Group. Also you can specify multiple items using semicolon ';' delimited
       -  Company administrator
    *  -  AdminEmail
       -  E-mail of the SharePoint administrator (for Office 365 only).
       -  admin@contoso.com
    *  -  AdminPassword
       -  Password of the SharePoint administrator (for Office 365 only).
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  https://contoso/SiteUrl
              [%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  Run as account of publisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/RevokePermissionOnWeb.png
   :alt: Remove Permissions from Site

Grant Permission on List
--------------------------------------------------
Grant specific permissions to an user on a list

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  Role Type
       -  permission levels:
                   * Full control
                   * Design
                   * Edit
                   * Contribute
                   * Read
                   * ViewOnly
                
       -  5
    *  -  List
       -  Title or Url of chosen list
       -  Tickets
    *  -  User or group
       -  Login, Email or Name of the User. Also you can specify multiple items using semicolon ';' delimited
       -  Workflow Context:Initiator
    *  -  AdminEmail
       -  E-mail of the SharePoint administrator (for Office 365 only).
       -  admin@contoso.com
    *  -  AdminPassword
       -  Password of the SharePoint administrator (for Office 365 only).
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  https://contoso/SiteUrl
              [%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  Run as account of publisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/GrantPermissionOnList.png
   :alt: Grant Permission on List

Remove Permissions from List
--------------------------------------------------
Delete specific permissions from an user on a list

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  Role Type
       -  permission levels:
                   * Full control
                   * Design
                   * Edit
                   * Contribute
                   * Read
                   * ViewOnly
                
       -  5
    *  -  List
       -  Title or Url of chosen list
       -  Tickets
    *  -  User or group
       -  Login, Email or Name of the User. Also you can specify multiple items using semicolon ';' delimited
       -  Jack@contoso.com
    *  -  AdminEmail
       -  E-mail of the SharePoint administrator (for Office 365 only).
       -  admin@contoso.com
    *  -  AdminPassword
       -  Password of the SharePoint administrator (for Office 365 only).
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  https://contoso/SiteUrl
             [%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  Run as account of publisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/RevokePermissionOnList.png
   :alt: Remove Permissions from List

Grant Permission on Item
--------------------------------------------------
Grant specific permissions to an user on an item

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  Role Type
       -  permission levels:
                   * Full control
                   * Design
                   * Edit
                   * Contribute
                   * Read
                   * ViewOnly
                
       -  5
    *  -  List
       -  Title or Url of chosen list
       -  Tickets
    *  -  Item
       -  Item ID
       -  44
    *  -  User or group
       -  Login, Email or Name of the User. Also you can specify multiple items using semicolon ';' delimited
       -  Jack@contoso.com
    *  -  AdminEmail
       -  E-mail of the SharePoint administrator (for Office 365 only).
       -  admin@contoso.com
    *  -  AdminPassword
       -  Password of the SharePoint administrator (for Office 365 only).
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  https://contoso/SiteUrl
             [%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  Run as account of publisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/GrantPermissionOnItem.png
   :alt: Grant Permission on Item

Remove Permissions from Item
--------------------------------------------------
Delete specific permissions from an user on item

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  Role Type
       -  permission levels:
                   * Full control
                   * Design
                   * Edit
                   * Contribute
                   * Read
                   * ViewOnly
                
       -  5
    *  -  List
       -  Title or Url of chosen list
       -  Tickets
    *  -  Item
       -  Item ID
       -  44
    *  -  User or group
       -  Login, Email or Name of the User. Also you can specify multiple items using semicolon ';' delimited
       -  Jack@contoso.com
    *  -  AdminEmail
       -  E-mail of the SharePoint administrator (for Office 365 only).
       -  admin@contoso.com
    *  -  AdminPassword
       -  Password of the SharePoint administrator (for Office 365 only).
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  https://contoso/SiteUrl
             [%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  Run as account of publisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/RevokePermissionOnItem.png
   :alt: Remove Permissions from Item

Restore Permissions Inheritance for Site
--------------------------------------------------
Remove unique permissions and restore permission inheritance on current SharePoint Site.

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  AdminEmail
       -  E-mail of the SharePoint administrator (for Office 365 only).
       -  admin@contoso.com
    *  -  AdminPassword
       -  Password of the SharePoint administrator (for Office 365 only).
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  https://contoso/SiteUrl
             [%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  Run as account of publisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/ResetPermissionOnWeb.png
   :alt: Restore Permissions Inheritance for Site

Restore Permissions inheritance for List
--------------------------------------------------
Remove unique permissions and restore permission inheritance on a SharePoint list

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  List
       -  Title or Url of chosen list
       -  Tickets
    *  -  AdminEmail
       -  E-mail of the SharePoint administrator (for Office 365 only).
       -  admin@contoso.com
    *  -  AdminPassword
       -  Password of the SharePoint administrator (for Office 365 only).
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  https://contoso/SiteUrl
             [%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  Run as account of publisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/ResetPermissionOnList.png
   :alt: Restore Permissions inheritance for List

Restore Permissions Inheritance for Item
--------------------------------------------------
Remove unique permissions and restore permission inheritance on a SharePoint Item

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  List
       -  Title or Url of chosen list
       -  Tickets
    *  -  Item
       -  Item ID
       -  44
    *  -  AdminEmail
       -  E-mail of the SharePoint administrator (for Office 365 only).
       -  admin@contoso.com
    *  -  AdminPassword
       -  Password of the SharePoint administrator (for Office 365 only).
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  https://contoso/SiteUrl
             [%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  Run as account of publisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/ResetPermissionOnItem.png
   :alt: Restore Permissions Inheritance for Item

Remove All Permissions from Site
--------------------------------------------------
Removing all user permissions from a SharePoint Site

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  AdminEmail
       -  E-mail of the SharePoint administrator (for Office 365 only).
       -  admin@contoso.com
    *  -  AdminPassword
       -  Password of the SharePoint administrator (for Office 365 only).
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  https://contoso/SiteUrl
              [%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  Run as account of publisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/DeleteAllPermissionsFromWeb.png
   :alt: Remove All Permissions from Web

Remove All Permissions from List
--------------------------------------------------
Removing all user permissions from a SharePoint List

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  List
       -  Title or Url of chosen list
       -  Tickets
    *  -  AdminEmail
       -  E-mail of the SharePoint administrator (for Office 365 only).
       -  admin@contoso.com
    *  -  AdminPassword
       -  Password of the SharePoint administrator (for Office 365 only).
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  https://contoso/SiteUrl
              [%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  Run as account of publisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/DeleteAllPermissionsFromList.png
   :alt: Remove All Permissions from List

Remove All Permissions from Item
--------------------------------------------------
Removing all user permissions from a SharePoint Item

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  List
       -  Title or Url of chosen list
       -  Tickets
    *  -  Item
       -  Item ID
       -  44
    *  -  AdminEmail
       -  E-mail of the SharePoint administrator (for Office 365 only).
       -  admin@contoso.com
    *  -  AdminPassword
       -  Password of the SharePoint administrator (for Office 365 only).
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  https://contoso/SiteUrl
             [%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  Run as account of publisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/DeleteAllPermissionsFromItem.png
   :alt: Remove All Permissions from Item

