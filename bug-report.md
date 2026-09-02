# Bug Report

## BUG-01 — Invalid authentication returns HTTP 200

### Description
When invalid username and password are sent to the authentication endpoint, the API returns HTTP status 200 instead of an authentication error status such as 401.

### Endpoint
POST /auth

### Test Data

```json
{
  "username": "wronguser",
  "password": "wrongpassword"
}
```

### Steps to Reproduce

1. Send a POST request to `/auth`.
2. Use invalid username and password.
3. Check the response status and body.

### Actual Result

HTTP Status:

`200 OK`

Response:

```json
{
  "reason": "Bad credentials"
}
```

### Expected Result

The API should return an authentication error status such as:

`401 Unauthorized`

with an appropriate error message.

### Severity

Low

### Priority

Low
