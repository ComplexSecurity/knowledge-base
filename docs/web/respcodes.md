HTTP status codes are codes returned by a [[server]] in response to a client's request. The codes are part of the HTTP response and indicate the status of the request. The codes are mainly divided into 5 categories:

- 1xx (Informational) - indicate a provisional response and are less common in daily use.
- 2xx (Successful) - indicate the client's request was successfully received, understood and accepted.
- 3xx (Redirection) - signify that further action needs to be taken by the client to complete the request.
- 4xx (Client Error) - represent errors made by the client.
- 5xx (Server Error) - indicate problems on the server's end.

Some of the most common HTTP status codes seen are:

| HTTP Status Code          | Description                                                                        |
| ------------------------- | ---------------------------------------------------------------------------------- |
| **200 OK**                    | Page has been fetched, action accepted and delivered to the client                 |
| **301 Permanent Redirect**    | Page requests has moved to a new URL which is permanent                            |
| **302 Temporary Redirect**    | Requested URL redirected to another website which is temporary                     |
| **304 Not Modified**          | Request not changed so client can resume the same cache in the future              |
| **400 Bad Request**           | Server not able to understand anything                                             |
| **401 Unauthorized**          | Requires user authentication                                                       |
| **403 Forbidden**             | Request understood, but refuses to fulfill it                                      |
| **404 Not Found**             | Request a URL and the server has not found anything                                |
| **500 Internal Server Error** | Requesting a URL is not fulfilled as the server encounters an unexpected condition |
| **501 Not Implemented**       | Server not able to recognize the request method and not able to support any resource                                                                                   |


