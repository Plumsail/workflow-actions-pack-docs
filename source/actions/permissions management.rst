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
    *  -  AdminLogin
       -  E-mail of the SharePoint administrator (for Office 365 only).
       -  :code:`admin@contoso.com`
    *  -  AdminPassword
       -  Password of the SharePoint administrator (for Office 365 only).
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  :code:`https://contoso/SiteUrl`
          [%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  Run as account of publisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: ../_static/img/addusertogroup.png
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
    *  -  AdminLogin
       -  E-mail of the SharePoint administrator (for Office 365 only).
       -  :code:`admin@contoso.com`
    *  -  AdminPassword
       -  Password of the SharePoint administrator (for Office 365 only).
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  :code:`https://contoso/SiteUrl`
          [%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  Run as account of publisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: ../_static/img/removeuserfromgroup.png
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
    *  -  AdminLogin
       -  E-mail of the SharePoint administrator (for Office 365 only).
       -  :code:`admin@contoso.com`
    *  -  AdminPassword
       -  Password of the SharePoint administrator (for Office 365 only).
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  :code:`https://contoso/SiteUrl`
          [%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  Run as account of publisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: ../_static/img/checkuseringroup.png
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
    *  -  AdminLogin
       -  E-mail of the SharePoint administrator (for Office 365 only).
       -  :code:`admin@contoso.com`
    *  -  AdminPassword
       -  Password of the SharePoint administrator (for Office 365 only).
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  :code:`https://contoso/SiteUrl`
          [%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  Run as account of publisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: ../_static/img/getmembersgroup.png
   :alt: Get Members of SharePoint Group

Set Default Site Group
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
    *  -  AdminLogin
       -  E-mail of the SharePoint administrator (for Office 365 only).
       -  :code:`admin@contoso.com`
    *  -  AdminPassword
       -  Password of the SharePoint administrator (for Office 365 only).
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  :code:`https://contoso/SiteUrl`
          [%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  Run as account of publisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: ../_static/img/changedefaultgroups.png
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
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  :code:`https://contoso/SiteUrl`
          [%Workflow Context:Current Site URL%]subSite
    *  -  User or group
       -  Login, Email or Name of the User or Group. Also you can specify multiple items using semicolon ';' delimited
       -  Workflow Context:Initiator
    *  -  AdminLogin
       -  E-mail of the SharePoint administrator (for Office 365 only).
       -  :code:`admin@contoso.com`
    *  -  AdminPassword
       -  Password of the SharePoint administrator (for Office 365 only).
       -  admin’sP@ssw0rd$
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  Run as account of publisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: ../_static/img/grantpermissiononweb.png
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
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  :code:`https://contoso/SiteUrl`
          [%Workflow Context:Current Site URL%]subSite
    *  -  User or group
       -  Login, Email or Name of the User or Group. Also you can specify multiple items using semicolon ';' delimited
       -  Company administrator
    *  -  AdminLogin
       -  E-mail of the SharePoint administrator (for Office 365 only).
       -  :code:`admin@contoso.com`
    *  -  AdminPassword
       -  Password of the SharePoint administrator (for Office 365 only).
       -  admin’sP@ssw0rd$
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  Run as account of publisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: ../_static/img/revokepermissiononweb.png
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
    *  -  AdminLogin
       -  E-mail of the SharePoint administrator (for Office 365 only).
       -  :code:`admin@contoso.com`
    *  -  AdminPassword
       -  Password of the SharePoint administrator (for Office 365 only).
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  :code:`https://contoso/SiteUrl`
          [%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  Run as account of publisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: ../_static/img/grantpermissiononlist.png
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
       -  :code:`Jack@contoso.com`
    *  -  AdminLogin
       -  E-mail of the SharePoint administrator (for Office 365 only).
       -  :code:`admin@contoso.com`
    *  -  AdminPassword
       -  Password of the SharePoint administrator (for Office 365 only).
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  :code:`https://contoso/SiteUrl`
          [%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  Run as account of publisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: ../_static/img/revokepermissiononlist.png
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
    *  -  Item
       -  Item ID
       -  44
    *  -  List
       -  Title or Url of chosen list
       -  Tickets
    *  -  User or group
       -  Login, Email or Name of the User. Also you can specify multiple items using semicolon ';' delimited
       -  :code:`Jack@contoso.com`
    *  -  AdminLogin
       -  E-mail of the SharePoint administrator (for Office 365 only).
       -  :code:`admin@contoso.com`
    *  -  AdminPassword
       -  Password of the SharePoint administrator (for Office 365 only).
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  :code:`https://contoso/SiteUrl`
          [%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  Run as account of publisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: ../_static/img/grantpermissiononitem.png
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
    *  -  Item
       -  Item ID
       -  44
    *  -  List
       -  Title or Url of chosen list
       -  Tickets
    *  -  User or group
       -  Login, Email or Name of the User. Also you can specify multiple items using semicolon ';' delimited
       -  :code:`Jack@contoso.com`
    *  -  AdminLogin
       -  E-mail of the SharePoint administrator (for Office 365 only).
       -  :code:`admin@contoso.com`
    *  -  AdminPassword
       -  Password of the SharePoint administrator (for Office 365 only).
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  :code:`https://contoso/SiteUrl`
          [%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  Run as account of publisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: ../_static/img/revokepermissiononitem.png
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
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  :code:`https://contoso/SiteUrl`
          [%Workflow Context:Current Site URL%]subSite
    *  -  AdminLogin
       -  E-mail of the SharePoint administrator (for Office 365 only).
       -  :code:`admin@contoso.com`
    *  -  AdminPassword
       -  Password of the SharePoint administrator (for Office 365 only).
       -  admin’sP@ssw0rd$
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  Run as account of publisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: ../_static/img/resetpermissiononweb.png
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
    *  -  AdminLogin
       -  E-mail of the SharePoint administrator (for Office 365 only).
       -  :code:`admin@contoso.com`
    *  -  AdminPassword
       -  Password of the SharePoint administrator (for Office 365 only).
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  :code:`https://contoso/SiteUrl`
          [%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  Run as account of publisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: ../_static/img/resetpermissiononlist.png
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
    *  -  Item
       -  Item ID
       -  44
    *  -  List
       -  Title or Url of chosen list
       -  Tickets
    *  -  AdminLogin
       -  E-mail of the SharePoint administrator (for Office 365 only).
       -  :code:`admin@contoso.com`
    *  -  AdminPassword
       -  Password of the SharePoint administrator (for Office 365 only).
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  :code:`https://contoso/SiteUrl`
          [%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  Run as account of publisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: ../_static/img/resetpermissiononitem.png
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
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  :code:`https://contoso/SiteUrl`
          [%Workflow Context:Current Site URL%]subSite
    *  -  AdminLogin
       -  E-mail of the SharePoint administrator (for Office 365 only).
       -  :code:`admin@contoso.com`
    *  -  AdminPassword
       -  Password of the SharePoint administrator (for Office 365 only).
       -  admin’sP@ssw0rd$
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  Run as account of publisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: ../_static/img/deleteallpermissionsfromweb.png
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
    *  -  AdminLogin
       -  E-mail of the SharePoint administrator (for Office 365 only).
       -  :code:`admin@contoso.com`
    *  -  AdminPassword
       -  Password of the SharePoint administrator (for Office 365 only).
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  :code:`https://contoso/SiteUrl`
          [%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  Run as account of publisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: ../_static/img/deleteallpermissionsfromlist.png
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
    *  -  Item
       -  Item ID
       -  44
    *  -  List
       -  Title or Url of chosen list
       -  Tickets
    *  -  AdminLogin
       -  E-mail of the SharePoint administrator (for Office 365 only).
       -  :code:`admin@contoso.com`
    *  -  AdminPassword
       -  Password of the SharePoint administrator (for Office 365 only).
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  :code:`https://contoso/SiteUrl`
          [%Workflow Context:Current Site URL%]subSite
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  Run as account of publisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: ../_static/img/deleteallpermissionsfromitem.png
   :alt: Remove All Permissions from Item

