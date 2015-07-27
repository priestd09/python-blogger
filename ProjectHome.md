# Python Blogger #

A python wrapper around the Blogger, Metaweblog, Wordpress, MovableType API

Author: `Ritesh Nadhani <riteshn@gmail.com>`

## Introduction ##

This library provides a pure python interface for the various blogging API.

Currently, only Metaweblog and Wordpress are implemented but it will be extended to use MovableType and Blogger soon. Since Blogger has now moved onto GData API, this interface will internally use GData API rather then XML-RPC.

## Installing/Building ##

Since this wrapper is just one Python (.py) file, no fancy installer or setup tools are provided. Just copy it to your project folder and you are good to go.

## Getting the code ##

View the trunk at:

> http://python-blogger.googlecode.com/svn/trunk/

Check out the latest development version anonymously with:

```
  $ svn checkout http://python-blogger.googlecode.com/svn/trunk/ python-blogger
```

## Using ##

```
	$ import pyblog
	$ blog = pyblog.WordPress('http://www.example.com/blog/xmlrpc.api', 'USERNAME', 'PASSWORD')
	$ print blog.get_recent_posts()
```

All return values are just standard Python based objects sent by xmlrpclib.

## Todo ##

Complete TO-DO list is available in the TO-DO page of the distribution

## Notes ##

pyblog.MetawWeblog objects implements all metaWeblog API as documented at http://www.xmlrpc.com/metaWeblogApi. The naming convention is similar to it except its more pythonic so getRecentPosts() becomes get\_recent\_posts(). For API, requiring struct parameter you will have to pass a dictionary with the corresponding key/value pair.

pyblog.Wordpress which extends pyblog.MetaWeblog implements the extra Wordpress XML-RPC methods. Currently, this API library fulfills all the functions provided with Wordpress v2.6

## More Information ##

Please visit http://groups.google.com/group/pyblog-devel for more discussion.

## License ##

```
      Complete info about BSD License: http://www.opensource.org/licenses/bsd-license.php
```