.. _VEA: http://www.verifyemailaddress.io

Features
========

> 99.9% Service Availability
----------------------------

Fully load balanced and automatic fail-over systems dispersed across 
multiple data centers in multiple regions deliver enterprise grade resilience.

See :doc:`reliability` for more information on availability and :term:`SLA`.

Fanatical Service Quality Management (SQM)
------------------------------------------
`VEA`_ operational staff obsessively monitor services to 
ensure the best possible uptime and coverage.

Uptime and functional correctness is actively monitored on a minute by 
minute basis from multiple data centers dispersed across North America, Europe and Asia.

Fast, Transparent Response Times
--------------------------------
Every query response includes stopwatch data that shows the time taken to execute the request.

Multi Factor Verification
-------------------------
Progressive verification using multiple verification processes including:

 * Syntax checking
 * DNS checking
 * Mailbox checking
 
Unrivalled Coverage
-------------------
With more than 5 years experience and the benefit of owning our own 
software stack, `VEA`_ has evolved its services to provide good coverage not only of the easier :term:`B2B` 
domains but also the more technically challenging :term:`B2C` domains including:

 * Hotmail
 * Yahoo
 * AOL
 * Yandex

Spam Trap Detection
-------------------
After many years R&D, `VEA`_ has developed technology  
that can effectively identify any probable :term:`Spam Trap`.

Disposable Email Address Detection
----------------------------------
Identify :term:`DEA` mail boxes.

Unrivalled Performance
----------------------
Strategic data centers in North America, Europe and Asia, aggressive 
caching and cloud based auto-scaling deliver outstanding performance. 
Typical queries are answered between 0.2 to 1.5 seconds.

.. note:: See :doc:`technical-spec`

On Screen Reporting
-------------------
Every account comes with a secure online portal for customers to 
view their current and historic usage via simple but powerful, user friendly charts and reports.

Thoughtful Versioning
---------------------
Endpoints are \"versioned\". This means that `VEA`_ 
can continue to release new functionality without \"breaking\" 
existing clients committed to integrating with our systems on legacy endpoints.

What it does
------------
`VEA`_ is used to check email addresses in real-time. 
Not only are syntax and domain checked, but that the user mailbox 
is available too. This is the only way to know for sure if an email address is valid.

Additionally identified as part of the email verification process 
is extra information including:

* :term:`DEA`.
* :term:`Spam Trap`.

How it works
------------
Email addresses are verified using various filters and processes. 
As a high level overview, an email address submitted for verification 
goes thorough the following filters:

Syntax
	A basic inspection of the syntax of the email address to see 
	if it looks valid. Work is done only using server :abbr:`CPU(Central Processing Unit)` 
	based on simple pattern matching algorithms.
	
DNS A
	Verifies a domain exists in :term:`DNS`. Domains that do not 
	exist in :term:`DNS` cannot have mail servers or email boxes.
	
	:term:`DNS` checks are performed over the network.
	
DNS MX
	Verify :term:`MX` records using :term:`DNS`. Domains that do not have 
	:term:`MX` records, have no mail servers and therefore no valid email boxes.
	
	:term:`MX` checks are performed over the network.

MailBox
	Verify email boxes with :term:`SMTP` checks.
	
	Connect to mail server and perform :term:`SMTP` 
	protocol to verify if mailbox exists.
	
	This is the deepest level of verification. It is 
	performed over the network.
