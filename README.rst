Recurly Python Client for Google App Engine (GAE)
=====================

This project is based on the [Recurly Python Client Library](https://github.com/recurly/recurly-client-python). It
replaces calls to _ssl and httplib2 with calls to Google App Engine's
[URL Fetch API](https://developers.google.com/appengine/docs/python/urlfetch/). This makes running the libary in
GAE's dev_appserver.py easier, and it lets you take advantage of Google's http fetching infrastructure.

Recurly's Python client library is an interface to its `REST API <http://docs.recurly.com/api>`_.

If you are not planning to deploy to GAE, you should use the official
[Recurly Python Client Library](https://github.com/recurly/recurly-client-python) instead.

Usage
-----

Set your API key and Recurly.js private key, and optionally set a certificate
authority certificate file and default currency::

   import recurly

   recurly.SUBDOMAIN = 'your-subdomain'
   recurly.API_KEY = '012345678901234567890123456789ab'
   recurly.js.PRIVATE_KEY = '0cc86846024a4c95a5dfd3111a532d13'

   # Set a certificate authority certs file to validate Recurly's certificate
   recurly.CA_CERTS_FILE = '/etc/pki/tls/certs/ca-bundle.crt'

   # Set a default currency for your API requests
   recurly.DEFAULT_CURRENCY = 'USD'


API Documentation
-----------------

Please see the `Recurly API <http://docs.recurly.com/api/>`_ for more information.

TODO
----
Unit tests are currently broken, as they expect a differently formatted response object. If you feel like contributing,
fork this repo and send a pull request.