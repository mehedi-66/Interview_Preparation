
// ****************** All about Status Code ********************

# HTTP Status Codes for APIs - Interview Guide

HTTP status codes are three-digit numbers that indicate the outcome of an HTTP request. In the context of APIs, understanding these status codes is crucial for communication between clients and servers.

## 1xx - Informational

- **100 - Continue:** The server acknowledges the request headers and informs the client to proceed with the request.

## 2xx - Success

- **200 - OK:** The request was successful, and the server provides the requested data.
- **201 - Created:** The request was successful, and a new resource was created.
- **204 - No Content:** The request was successful, but there is no additional information to send.

## 3xx - Redirection

- **301 - Moved Permanently:** The requested resource has been permanently moved to a new location.
- **302 - Found:** The requested resource has been temporarily moved to a different location.
- **304 - Not Modified:** The client's cached copy is still valid, and there is no need to send a new request.

## 4xx - Client Errors

- **400 - Bad Request:** The server cannot process the request due to a client error, e.g., malformed request syntax.
- **401 - Unauthorized:** Authentication is required, and the credentials provided are not valid.
- **403 - Forbidden:** The client does not have permission to access the requested resource.
- **404 - Not Found:** The requested resource could not be found on the server.
- **422 - Unprocessable Entity:** The server understands the request, but it cannot process it due to semantic errors.

## 5xx - Server Errors

- **500 - Internal Server Error:** A generic error message indicating an unexpected condition that prevented the server from fulfilling the request.
- **502 - Bad Gateway:** The server, while acting as a gateway or proxy, received an invalid response from an upstream server.
- **503 - Service Unavailable:** The server is not ready to handle the request. Common causes include overloading or maintenance.
- **504 - Gateway Timeout:** The server, while acting as a gateway or proxy, did not receive a timely response from an upstream server.

Understanding these HTTP status codes is essential for troubleshooting, debugging, and designing robust APIs. In an interview, be prepared to explain scenarios in which each code might be encountered and how to handle them appropriately.
