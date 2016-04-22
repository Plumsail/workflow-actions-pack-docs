String processing (Free)
==================================================


Split string
--------------------------------------------------
The workflow action splits string into collection of substrings using separator string.

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  SourceDate
       -  Source string
       -  test1;test2;test3;test4
    *  -  SplitString
       -  Separator string
       -  ``;``


Output parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  ResultVariable
       -  Specify dictionary workflow variable to store collection of substrings.
       -  Dictionary variable with following structure::

            [
              "test1",
              "test2",
              "test3",
              "test4"
            ]                   


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/SplitStringActionExample.png
   :alt: Split string workflow action example

Join Dictionary Values
--------------------------------------------------
Concatenate the values of dictionary into single string

Output parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  Result string
       -  String value will constain result of operation
       -  ``/lib1/Order1.docx;/lib2/Order2.docx``


Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  Source dictionary
       -  Data source, type dictionary
       -  Variable:Attachments
    *  -  Separator
       -  Separator that will be used for string concatenation
       -  ';' or any of symbols or string
    *  -  Path
       -  Key for select or path
       -  ``({0})/ServerRelativeUrl``


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/DynamicValueJoinToString.png
   :alt: Join Dictionary Values

 
Format date
--------------------------------------------------
The workflow action formats date using specified format string.

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  SourceDate
       -  Date to format
       -  3/21/2014 7:27:10 PM
    *  -  FormatString
       -  Format string. The workflow action uses .NET method DateTime.ToString(string format), you can find possible format strings on MSDN:

          * `Standard Date and Time Format Strings <http://msdn.microsoft.com/library/az4se3k1%28v=vs.110%29.aspx>`_
          * `Custom Date and Time Format Strings <http://msdn.microsoft.com/en-us/library/8kb3ddd4%28v=vs.110%29.aspx>`_

       -  :: 

              d  
              D  
              MMM  
              d MMMM  
              ddd d MMM


Output parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  ResultString
       -  Specify workflow variable to formatted string
       -  Friday 29 August


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/FormatDateActionExample.png
   :alt: Format date workflow action example

 
Get length of string
--------------------------------------------------
The workflow action returns length of a string.

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  SourceString
       -  Source string
       -  test string


Output parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  ResultVariable
       -  Specify workflow variable to store length
       -  11


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/GetLengthOfStringExample.png
   :alt: Get length of string workflow action example

 
String contains
--------------------------------------------------
The workflow action checks if a string contains a substring. It allows optionally ignore case of the source string and the substing.

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  IgnoreCase
       -  Allows to ignore case of the source string and of the substring. Default value: Yes.
       -  Yes  No
    *  -  SourceString
       -  Source string
       -  test string
    *  -  Substring
       -  Substring
       -  test


Output parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  ResultVariable
       -  Specify workflow variable to store result.
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/StringContainsActionExample.png
   :alt: String contains workflow action example

 
String starts with
--------------------------------------------------
The workflow action checks if a string starts with a substring. It allows optionally ignore case of the source string and the substing.

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  IgnoreCase
       -  Allows to ignore case of the source string and of the substring. Default value: Yes.
       -  Yes  No
    *  -  SourceString
       -  Source string
       -  test string
    *  -  Substring
       -  Substring
       -  te


Output parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  ResultVariable
       -  Specify workflow variable to store result.
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/StringStartsWithActionExample.png
   :alt: String starts with workflow action example

 
String ends with
--------------------------------------------------
The workflow action checks if a string ends with a substring. It allows optionally ignore case of the source string and the substing.

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  IgnoreCase
       -  Allows to ignore case of the source string and of the substring. Default value: Yes.
       -  Yes  No
    *  -  SourceString
       -  Source string
       -  test string
    *  -  Substring
       -  Substring
       -  ing


Output parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  ResultVariable
       -  Specify workflow variable to store result.
       -  Yes


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/StringEndsWithActionExample.png
   :alt: String ends with workflow action example

 
String to lower
--------------------------------------------------
The workflow action transforms a string to lower case.

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  SourceString
       -  Source string
       -  TEST STRING


Output parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  ResultVariable
       -  Specify workflow variable to store lower string.
       -  test string


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/StringToLowerActionExample.png
   :alt: String to lower workflow action example

 
String to upper
--------------------------------------------------
The workflow action transforms a string to upper case.

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  SourceString
       -  Source string
       -  test string


Output parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  ResultVariable
       -  Specify workflow variable to store upper string
       -  TEST STRING


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/StringToUpperActionExample.png
   :alt: String to upper workflow action example

