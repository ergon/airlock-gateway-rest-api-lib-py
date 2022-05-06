# airlock-gateway-rest-api-lib-py

Library for easier use of Airlock's REST API.

This library is not part of the official Airlock product delivery and
Ergon/Airlock does not provide support for it. Best effort support may
be provided by the contributor of the library.

This library uses the `requests` library to perform standard HTTP requests
to Airlock Gateway REST endpoints.

404 response status codes are handled by this library, i.e. if a provided ID
or REST endpoint cannot be found, no exceptions will be raised.

For all other unexpected response status codes, e.g. malformed data is used to
generate a new mapping, a custom Exception named `AirlockGatewayRestError` is
raised.

In addition to that, any Exception raised by the `requests` library is not
handled by this library, so for example if network problems occur,
multiple Errors will be raised by the underlying library.

An example script is provided under [Airlock's example script repository](https://github.com/ergon/airlock-example-scripts)
with the intent to demonstrate how to use some of the library functions.

A full documentation of this library is available at [Airlock's GitHub Page](https://ergon.github.io/airlock-gateway-rest-api-lib).