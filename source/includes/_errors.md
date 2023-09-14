# Errors

The s-aws-api API uses the following error codes:


Error Code | Meaning
---------- | -------
400 | Bad Request -- Your request is invalid.
401 | Unauthorized -- Unauthorized or invalid client application credentials.
403 | Forbidden -- The aws requested is hidden for administrators only.
404 | Not Found -- The specified information could not be found.
500 | Internal Server Error -- Bad response from authorization server, or WSDL SOAP Fault error
503 | Service Unavailable -- We're temporarily offline for maintenance. Please try again later.
