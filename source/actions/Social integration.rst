Social integration
==================================================


Publish to Wordpress
--------------------------------------------------
Publish a blog post with the given title, content, categories and tags.

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  WPBody
       -  Text with content of blog post (may contain HTML)
       -  <h1>Quarterly report...</h1>
    *  -  WPTitle
       -  Title of the blog post
       -  Quarterly Results
    *  -  WPCategies
       -  Comma-separated list of categories of the blog post
       -  Articles, news
    *  -  WPTags
       -  Comma-separated list of tags of the blog post
       -  Market research, our product
    *  -  WPUrl
       -  URL of the blog site or URL to xmlrpc.php
       -  ``http://blog.contoso.com/xmlrpc.php``
    *  -  WPLogin
       -  Wordpress username (requires permission to create new posts in blog)
       -  SPPublish
    *  -  WPPassword
       -  Wordpress password
       -  P@ssw0rd$=)


Output parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  URLToPost
       -  Specify workflow variable to store blog post URL.
          type: string
       -  ``http://blog.contoso.com/Corpotate-news``


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/PublishToWordpress.png
   :alt: 

Post to MicroFeed
--------------------------------------------------
Publishes specific message on user's micro feed.

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  Message
       -  Text of the message
       -  I approved a sales report
    *  -  UserEmail
       -  E-mail of the SharePoint Online User
       -  JackDaniels@contoso.com
    *  -  UserPassword
       -  Password of the SharePoint Online User
       -  Jack’sP@ssw0rd


Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/PublishFeed.png
   :alt: 

Post to Twitter
--------------------------------------------------
Posts message to twitter

Input parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. list-table::
    :header-rows: 1
    :widths: 10 30 20

    *  -  Parameter
       -  Description
       -  Example
    *  -  TweetText
       -  Text of the tweet
       -  Sales report has been approved by Mike
    *  -  ConsumerKey
       -  To obtain Twitter's keys you have to register a dev account on dev.twitter.com. You can get more information in the following  video: http://www.youtube.com/watch?v=pRrUYxn5CeYPlease, check that your application has read and write permissions.
       -  Jc1BMOTkachta185W9aoWA
    *  -  ConsumerSecret
       -
       -  Sales_Department
    *  -  AccessToken
       -
       -  ``1965200054-gmnOECnAuWkYIkWUr4vrD0Y4p3WB0E8YpRYD42q``
    *  -  AccessTokenSecret
       -
       -  ``ayADJaBS5sdPM848FqmikvRwzGTpO4udi4kVVUFg``

Example
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. image:: /_static/img/PublishToTwitter.png
   :alt: 

