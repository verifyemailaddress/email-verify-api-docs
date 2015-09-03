.. _account: https://register.verifyemailaddress.io/signup
.. _portal: https://verifyemail.azurewebsites.net

Quick Start
===========

This quick start guide is designed to get you up and running as fast as possible.

Please follow the steps below in sequence:

1) Create Account
-----------------
Create your `account`_.

2) Login
--------
Login to your customer `portal`_ to retrieve your :term:`API` :term:`License Key`.

3) Try it
---------
Plug your license key into the following 

::

	https://api1.27hub.com/api/emh/a/v2?k=INSERTYOURLICENSEKEY&e=john.doe@gmail.com
	
Paste the url above into your browser and watch the response come back as follows:

::

	{
		"result": "Bad",
		"reason": "MailboxDoesNotExist",
		"role": false,
		"free": true,
		"disposable": false,
		"email": "john.doe@gmail.com",
		"domain": "gmail.com",
		"user": "john.doe",
		"mailServerLocation": "US",
		"duration": 723
	}

.. note:: 	Internet Explorer may prompt to download the file instead of simply displaying it on screen. 
			This is a quirk of Internet Explorer and not an issue with the :term:`API`.
			We do not recommend Internet Explorer for testing with the :term:`API`. Instead, use
			Chrome or Firefox - both will display the results on screen correctly!
