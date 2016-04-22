SharePoint Utils 
==================================================


Start a List Workflow (2013)
--------------------------------------------------
Start a list level workflow and pass input parameters, if they were specified
Attention! The workflow action can run only 2013 workflows, to run 2010 workflow you can use `Coordination actions <http://blogs.msdn.com/b/sharepointdesigner/archive/2012/08/18/how-to-trigger-a-sharepoint-2010-workflow-from-a-sharepoint-2013-workflow.aspx>`_

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  Workflow name
       -  Name of the workflow which will be started
       -  Send notifications
    *  -  Item ID
       -  Item ID
       -  44 or [Variable:ItemId]
    *  -  List name
       -  Title, Url or guid of list
       -  Clients
    *  -  Input parameters
       -  Dictionary that contains input parameters for workflow
       -  [Variable:InputParameters]
    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  https://contoso/SiteUrl
          [%Workflow Context:Current Site URL%]subSite      
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  RunAsPublisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes

Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/StartListWorkflow.png
   :alt: Start a List Workflow (2013)


Start a Site Workflow (2013)
--------------------------------------------------
Start a site level workflow and pass input parameters, if they were specified
Attention! The workflow action can run only 2013 workflows, to run 2010 workflow you can use `Coordination actions <http://blogs.msdn.com/b/sharepointdesigner/archive/2012/08/18/how-to-trigger-a-sharepoint-2010-workflow-from-a-sharepoint-2013-workflow.aspx>`_

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  Workflow name
       -  Name of the workflow which will be started
       -  Send notifications
    *  -  Input parameters
       -  Dictionary that contains input parameters for workflow
       -  [Variable:InputParameters]
    *  -  AdminLogin
       -  The login of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin@contoso.com
    *  -  AdminPassword
       -  The password of the user who has appropriate permissions to perform operation. This parameter doesn't exist in the version for SharePoint 2013 on-premise.
       -  admin’sP@ssw0rd$
    *  -  SiteUrl
       -  The URL of the current SharePoint site. This property defines context of the workflow action. All actions performed by workflow action will be executed on specified SharePoint site. If this property is blank it will use current SharePoint site by default.
       -  https://contoso/SiteUrl
          [%Workflow Context:Current Site URL%]subSite
                
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  RunAsPublisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/StartSiteWorkflow.png
   :alt: Start a Site Workflow (2013)

Get Site Option Value as String
--------------------------------------------------
Read string value from Site Options (Property Bag)

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  Property Name
       -  Name of property
       -  PortalSettings
          [Variable:SettingsKey]
                
    *  -  Property Value
       -  Output string value
       -  [Variable:ResultString]


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/GetStringProperty.png
   :alt: Get Site Option Value as String

Get Site Option Value as Dictionary
--------------------------------------------------
Read json value from Site Options (Property Bag) and save it to Dictionary variable

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  Property Name
       -  Name of property
       -  PortalSettings
          [Variable:SettingsKey] 
    *  -  Property Value
       -  Output dictionary value
       -  [Variable:ResultDictionary]


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/GetDictionaryProperty.png
   :alt: Get Site Option Value as Dictionary

Evaluate expression
--------------------------------------------------
Evaluate mathematical expressions and save result to Dictionary with Resultas key
We use `NCalc <https://ncalc.codeplex.com/>`_ framework as mathematical expressions evaluator. You can use it to evaluate logical or arithmetical expressions. For example ``2 * 2 or if(3 % 2 = 1, true, false)``. This workflow action can help you to calculate complex formulas as well as evaluate complex logical expressions.

To get more informaiton about available operators, values and functions visit following links:

* `Operators <https://ncalc.codeplex.com/wikipage?title=operators&referringTitle=Home>`_
* `Values <https://ncalc.codeplex.com/wikipage?title=values&referringTitle=Home>`_
* `Functions <https://ncalc.codeplex.com/wikipage?title=functions&referringTitle=Home>`_

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  Expression
       -  Expression for evaluation
       -  ::

              2+2*2
              sqrt(9)
              sin(1)
              true or false = true

    *  -  OutputResult
       -  Dictionary that contains output result in "Result" key
       -  ``[Variable:ResultDictionary]``
    *  -  ThrowError
       -  Detects whether workflow should be interrupted in case of error or not.
       -  Yes
    *  -  RunAsPublisher
       -  Run under user account who published workflow (for OnPremise only)
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/EvaluateExpression.png
   :alt: Evaluate expression

Parse XML to Dictionary
--------------------------------------------------
The workflow action receives XML string and convert it to a Dictionary. 

Output parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  Result dictionary
       -  Output dictionary value. Please check out the following article to know more.
          How to work with dictionaries in SharePoint 2013 and Office 365 workflow
       -  ::

            {
               "recurrence":{
                  "rule":{
                     "firstDayOfWeek":"su",
                     "repeat":{
                        "daily":{
                           "@dayFrequency":"1"
                        }
                     },
                     "repeatInstances":"10"
                  }
               }
            }


Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  Input string 
       -  Input XML string
       -  ::

            <recurrence>
                <rule>
                    <firstDayOfWeek>su</firstDayOfWeek>
                    <repeat>
                        <daily dayFrequency="1" />
                    </repeat>
                    <repeatInstances>10</repeatInstances>
                </rule>
            </recurrence>

Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/ParseXMLWorkflowAction.png
   :alt: Parse XML to Dictionary

