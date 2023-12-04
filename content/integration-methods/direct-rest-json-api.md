## REST/JSON API Integration

This page would contain information specific to integrating directly to the REST/JSON APIs (Application Programming Interfaces)

Merchants would use this approach if they want build integrations directly to our Payment APIs **without** using our SDKs.

Fundamentally, they will need to:

* use the documentation to understand the structure of the request & response payloads.
* Optionally download an OpenAPI file and use it to code generate strongly typed data objects (that serialize/deserialize) into the request & response payloads.  
<br/>
* build a JSON payload
* add it as the body of a HTTP request
* add the necessary HTTP headers
* POST it to the appropriate endpoint
<br/>
* accept the response
* inspect the HTTP response code
* Interpret the response payload (whose type depends on the response code)