Azure AD Administration 
==================================================


Create Azure AD User
--------------------------------------------------
Creates a new user in Windows Azure Active Directory.

Output parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  Result properties
       -  Returns the dictionary with properties of the user. You can find the full list of properties at `MSDN <http://msdn.microsoft.com/en-us/library/azure/dn194133.aspx>`_.                  
          You can get separate property from dictionary using the workflow action ‘Get an Item from a Dictionary’. See the picture with example under input parameters.
        
          To understand Dictionary type read this `MSDN article <http://msdn.microsoft.com/en-us/library/office/jj554504%28v=office.15%29.aspx>`_.
          Dictionary containing user properties. You can find the full list of properties at
                
       -  The structure of the dictionary with key value pairs::

            FirstName  : "John"
            LastName   : "Davis"
            DisplayName: "John Davis"
            MobilePhone: "+1 443 4344555"
            Office     : "505"
            ...



Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  User principal name
       -  The principal name for the user.
       -  john.davis@plumsail.com
    *  -  Display Name
       -  The display name of the user.
       -  John Davis
    *  -  FirstName
       -  The first name of the user.
       -  John
    *  -  LastName
       -  The last name of the user.
       -  Davis
    *  -  Password
       -  The password for the user. If this value is empty, then random password will be generated. This workflow action returns dictionary with properties of the new user. You will be able to get generated password from this dictionary.
       -  Empty or something like P@$$w0rd33
    *  -  AlternateEmailAddresses
       -  The alternate email addresses of the user.
       -  john.davis@gmail.com
    *  -  City
       -  The city of the user.
       -  New York
    *  -  Country
       -  The country of the user.
       -  USA
    *  -  Department
       -  The department of the user.
       -  IT Department
    *  -  Fax
       -  The fax number of the user.
       -  +1 334 634221
    *  -  LicenseAssignment
       -  The SKU code for Office 365 subscription. You can get it using PowerShell. You can find example of PowerShell script in `this article <https://plumsail.com/blog/2014/06/how-to-automatically-create-office-365-user-accounts-using-sharepoint-workflow/>`_.
       -  Plumsail:Enterprise
    *  -  MobilePhone
       -  The mobile phone number of the user.
       -  +1 244 23454534
    *  -  Office
       -  The office of the user.
       -  505
    *  -  PhoneNumber
       -  The phone number of the user.
       -  +1 244 23454534
    *  -  PostalCode
       -  The postal code of the user.
       -  33701
    *  -  PreferredLanguage
       -  The preferred language of the user.
       -  US
    *  -  State
       -  The state where the user is located.
       -  FL
    *  -  StreetAddress
       -  The street address of the user.
       -  Bay Pines Blvd
    *  -  Title
       -  The title of the user.
       -  Manager
    *  -  UsageLocation
       -  The location of the user where services are consumed. Must be a two-letter country code.
       -  US
    *  -  PasswordNeverExpires
       -  Sets whether or not the user's password will expire periodically.
       -  True
    *  -  StrongPasswordRequired
       -  Sets whether or not the user requires a strong password.
       -  False
    *  -  BlockCredential
       -  When true, the user will not be able to log on using their user ID.
       -  False
    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  ``https://contoso/SiteUrl[%Workflow Context:Current Site URL%]subSite``
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  RunAsPublisher
       -  Detects whether the workflow action has to be runned under the user account who published the workflow (for SharePoint 2013 on-premise only).
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/NewMsolUser.png
   :alt: Create Azure AD User

Remove Azure AD User
--------------------------------------------------
Removes the user from Windows Azure Active Directory.

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  User principal name
       -  The user ID of the user to remove.
       -  john.davis@plumsail.com
    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  ``https://contoso/SiteUrl[%Workflow Context:Current Site URL%]subSite``
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  RunAsPublisher
       -  Detects whether the workflow action has to be runned under the user account who published the workflow (for SharePoint 2013 on-premise only).
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/RemoveMsolUser.png
   :alt: Remove Azure AD User

Update Azure AD User
--------------------------------------------------
Updates a user in Windows Azure Active Directory.

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  User principal name
       -  The principal name for the user.
       -  john.davis@plumsail.com
    *  -  DispName
       -  The display name of the user.
       -  John Davis
    *  -  FirstName
       -  The first name of the user.
       -  John
    *  -  LastName
       -  The last name of the user.
       -  Davis
    *  -  Password
       -  The password for the user. If this value is empty, then random password will be generated. This workflow action returns dictionary with properties of the new user. You will be able to get generated password from this dictionary.
       -  Empty or something like P@$$w0rd33
    *  -  AlternateEmailAddresses
       -  The alternate email addresses of the user.
       -  john.davis@gmail.com
    *  -  City
       -  The city of the user.
       -  New York
    *  -  Country
       -  The country of the user.
       -  USA
    *  -  Department
       -  The department of the user.
       -  IT Department
    *  -  Fax
       -  The fax number of the user.
       -  +1 334 634221
    *  -  LicenseAssignment
       -  The SKU code for Office 365 subscription. You can get it using PowerShell. You can find example of PowerShell script in `this article <https://plumsail.com/blog/2014/06/how-to-automatically-create-office-365-user-accounts-using-sharepoint-workflow/>`_.
       -  Plumsail:Enterprise
    *  -  MobilePhone
       -  The mobile phone number of the user.
       -  +1 244 23454534
    *  -  Office
       -  The office of the user.
       -  505
    *  -  PhoneNumber
       -  The phone number of the user.
       -  +1 244 23454534
    *  -  PostalCode
       -  The postal code of the user.
       -  33701
    *  -  PreferredLanguage
       -  The preferred language of the user.
       -  US
    *  -  State
       -  The state where the user is located.
       -  FL
    *  -  StreetAddress
       -  The street address of the user.
       -  Bay Pines Blvd
    *  -  Title
       -  The title of the user.
       -  Manager
    *  -  UsageLocation
       -  The location of the user where services are consumed. Must be a two-letter country code.
       -  US
    *  -  PasswordNeverExpires
       -  Sets whether or not the user's password will expire periodically.
       -  True
    *  -  StrongPasswordRequired
       -  Sets whether or not the user requires a strong password.
       -  False
    *  -  BlockCredential
       -  When true, the user will not be able to log on using their user ID.
       -  False
    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  `https://contoso/SiteUrl[%Workflow Context:Current Site URL%]subSite`
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  RunAsPublisher
       -  Detects whether the workflow action has to be runned under the user account who published the workflow (for SharePoint 2013 on-premise only).
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/SetMsolUser.png
   :alt: Update Azure AD User

Get properties from Azure AD user
--------------------------------------------------
Gets the dictionary with properties of specified user from Windows Azure Active Directory.

Output parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  Result properties
       -  Returns the dictionary with properties of the user. You can find the full list of properties at `MSDN <http://msdn.microsoft.com/en-us/library/azure/dn194133.aspx>`_.                  
          You can get separate property from dictionary using the workflow action ‘Get an Item from a Dictionary’. See the picture with example under input parameters.
        
          To understand Dictionary type read this `MSDN article <http://msdn.microsoft.com/en-us/library/office/jj554504%28v=office.15%29.aspx>`_.
          Dictionary containing user properties. You can find the full list of properties at
                
       -  The structure of the dictionary with key value pairs::

            FirstName  : "John"
            LastName   : "Davis"
            DisplayName: "John Davis"
            MobilePhone: "+1 443 4344555"
            Office     : "505"
            ...



Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  User principal name
       -  The user ID of the user to retrieve.
       -  john.davis@plumsail.com
    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  ``https://contoso/SiteUrl[%Workflow Context:Current Site URL%]subSite``
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  RunAsPublisher
       -  Detects whether the workflow action has to be runned under the user account who published the workflow (for SharePoint 2013 on-premise only).
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/GetMsolUser.png
   :alt: Get properties from Azure AD user

Assign License to Azure AD User
--------------------------------------------------
Add the license assignment for a user.

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  User principal name
       -  The user ID of the user to update.
       -  john.davis@plumsail.com
    *  -  License
       -  A license to assign to the user.
       -  Plumsail:enterprise
    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  ``https://contoso/SiteUrl[%Workflow Context:Current Site URL%]subSite``
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  RunAsPublisher
       -  Detects whether the workflow action has to be runned under the user account who published the workflow (for SharePoint 2013 on-premise only).
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/AddMsolUserLicense.png
   :alt: Assign License to Azure AD User

Remove License from Azure AD User
--------------------------------------------------
Remove the license assignment for a user.

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  User principal name
       -  The user ID of the user to update.
       -  john.davis@plumsail.com
    *  -  License
       -  A license to remove from the user.
       -  Plumsail:Enterprise
    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  ``https://contoso/SiteUrl[%Workflow Context:Current Site URL%]subSite``
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  RunAsPublisher
       -  Detects whether the workflow action has to be runned under the user account who published the workflow (for SharePoint 2013 on-premise only).
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/RemoveMsolUserLicense.png
   :alt: Remove License from Azure AD User

Reset Password for Azure AD User
--------------------------------------------------
Resets the password for a user.

Output parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  GeneratedPassword
       -  The password generated for the user. This is output variable
       -  


Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  User principal name
       -  The user ID of the user to set the password for.
       -  john.davis@plumsail.com
    *  -  ForceChangePassword
       -  When true, the user will be required to change their password the next time they sign in.
       -  True
    *  -  NewPassword
       -  The password for the user. If this value is empty, then random password will be generated. This workflow action returns dictionary with properties of the new user. You will be able to get generated password from this dictionary.
       -  Empty or something like P@$$w0rd33
    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  ``https://contoso/SiteUrl[%Workflow Context:Current Site URL%]subSite``
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  RunAsPublisher
       -  Detects whether the workflow action has to be runned under the user account who published the workflow (for SharePoint 2013 on-premise only).
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/SetMsolUserPassword.png
   :alt: Reset Password for Azure AD User

Create Azure AD Group
--------------------------------------------------
Adds a new group to the Windows Azure Active Directory.

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  GroupName
       -  The display name of the group.
       -  Helpdesk contributors
    *  -  GroupDescription
       -  The description of the group.
       -  Can read, write and create new content
    *  -  ManagedBy
       -  The owner of the group.
       -  administrator@contoso.com
    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  ``https://contoso/SiteUrl[%Workflow Context:Current Site URL%]subSite``
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  RunAsPublisher
       -  Detects whether the workflow action has to be runned under the user account who published the workflow (for SharePoint 2013 on-premise only).
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/NewMsolGroup.png
   :alt: Create Azure AD Group

Remove Azure AD Group
--------------------------------------------------
Removes a group from Windows Azure Active Directory.

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  GroupName
       -  The display name or the unique ID of the group to remove.
       -  Helpdesk contributors
    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  ``https://contoso/SiteUrl[%Workflow Context:Current Site URL%]subSite``
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  RunAsPublisher
       -  Detects whether the workflow action has to be runned under the user account who published the workflow (for SharePoint 2013 on-premise only).
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/RemoveMsolGroup.png
   :alt: Remove Azure AD Group

Add User to Azure AD Group
--------------------------------------------------
Adds a member to an existing security group.

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  User principal name
       -  The User principal name or the unique ID of the user to add.
       -  john.davis@plumsail.com
    *  -  GroupName
       -  The display name or the unique ID of the group.
       -  Helpdesk contributors
    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  ``https://contoso/SiteUrl[%Workflow Context:Current Site URL%]subSite``
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  RunAsPublisher
       -  Detects whether the workflow action has to be runned under the user account who published the workflow (for SharePoint 2013 on-premise only).
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/AddMsolGroupMember.png
   :alt: Add User to Azure AD Group

Remove User from Azure AD Group
--------------------------------------------------
Removes a member from a security group.

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  User principal name
       -  The User principal name or the unique ID of the user to remove.
       -  john.davis@plumsail.com
    *  -  GroupName
       -  The display name or the unique ID of the group.
       -  Helpdesk contributors
    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  ``https://contoso/SiteUrl[%Workflow Context:Current Site URL%]subSite``
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  RunAsPublisher
       -  Detects whether the workflow action has to be runned under the user account who published the workflow (for SharePoint 2013 on-premise only).
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/RemoveMsolGroupMember.png
   :alt: Remove User from Azure AD Group

