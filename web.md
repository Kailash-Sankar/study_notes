# Web Development

  - HTTP
    - GET : retreive data from a server at the specified resource
    - POST : send data to the API sever to create or udpate a resource. Non-idempotent.
    - PUT : send data to the API to create or update a resource. Idempotent, i.e calling the same PUT request multiple times will always produce the same result
    - HEAD :  useful for checking what a GET request will return. Such a request can be done before deciding to download a large resource to save bandwidth, for example.
    - DELETE : delete the specified resource.
    - PATCH : only apply partial modifications to the resource. Non-idempotent
    - OPTIONS : return data describing what other methods and operations the server supports at the given URL
  - Status Codes
    - 200 : OK
    - 301 : Moved Permanently
    - 400 : Bad Request
    - 401 : Unauthorized
    - 404 : Not Found
    - 500 : Internal Server Error
  - RESTful API
  - Authentication
    - OAuth
  - Headers
    - content-type
    - accept

#### Links
* https://assertible.com/blog/7-http-methods-every-web-developer-should-know-and-how-to-test-them
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/201
* https://martinfowler.com/articles/richardsonMaturityModel.html
* https://webmasters.stackexchange.com/questions/31212/difference-between-the-accept-and-content-type-http-headers
