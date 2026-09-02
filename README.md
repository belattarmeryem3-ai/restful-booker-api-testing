# Restful Booker API Testing Portfolio

API testing project created with **Postman** using the Restful Booker API.

The goal of this project is to demonstrate practical API testing skills including CRUD operations, authentication, test automation, negative testing, test case documentation, and bug reporting.

## Tools

- Postman
- REST API
- JavaScript
- GitHub

## API Under Test

Restful Booker API

## Test Coverage

The project covers the following scenarios:

- Authentication with valid credentials
- Create a new booking
- Get booking by ID
- Update an existing booking
- Verify updated booking data
- Delete a booking
- Verify deleted booking
- Authentication with invalid credentials
- Get a non-existing booking
- Update booking without authentication

## Automated Tests

Postman scripts are used to validate:

- HTTP status codes
- Response data
- Response data types
- Booking IDs
- Authentication tokens
- Updated values
- Error responses

Collection variables are used to dynamically store and reuse:

- `token`
- `bookingId`

This allows requests to be chained together without using hard-coded booking IDs.

## Test Results

| Total Test Cases | Passed | Failed |
|---|---|---|
| 10 | 10 | 0 |

## Bug Found

### Invalid Authentication Returns HTTP 200

When invalid credentials are sent to the authentication endpoint, the API returns:

`200 OK`

with:

```json
{
  "reason": "Bad credentials"
}
```

A more appropriate HTTP response would be `401 Unauthorized`.

Full details are available in `bug-report.md`.

## Project Files

- `test-cases.md` — Test cases and execution results
- `test-summary.md` — Test summary report
- `bug-report.md` — Documented API issue
- `Project 03 - API Testing Portfolio.postman_collection.json` — Postman collection

## Skills Demonstrated

- REST API Testing
- CRUD Testing
- Authentication Testing
- Positive & Negative Testing
- Postman Test Automation
- JavaScript Assertions
- Dynamic Variables
- API Test Documentation
- Bug Reporting
- Git & GitHub
