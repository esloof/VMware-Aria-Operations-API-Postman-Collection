# VMware-Aria-Operations-API-Postman-Collection

In this article, I’ll describe how to connect to the REST API of VMware Aria Operations. I’ll also demonstrate how to use the Swagger UI to construct API entries in Postman.
The initial access to the AriaOps API is based on authentication with a username, password and authentication source provided in a JSON body. Don’t try to do this with basic authentication, because it will fail. Simply construct a POST call with a JSON body, get the ops:token. This token is needed for any subsequent REST calls against AriaOps.
After receiving a 200 (OK) response. The ops:token has successfully been retrieved. It will expire after 6 hours. Any subsequent requests must include this token.
To construct new API calls, you can use either the API-Programming-Operations Guide or the Swagger UI. In the Swagger UI, it is fairly easy to test API calls with the “Try it out” feature.
This also includes a valid ops:token in the test request. You can copy the Curl request from Swagger and paste it into a new request in Postman. This automatically translates the curl request into a valid REST API call, and automaticly fills all the parameters and creates a valid JSON body.
