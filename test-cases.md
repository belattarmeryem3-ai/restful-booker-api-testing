| ID    | Test Case                             | Expected Result       | Actual Result          | Status |
| ----- | ------------------------------------- | --------------------- | ---------------------- | ------ |
| TC-01 | Generate token with valid credentials | 200 + token           | 200 + token            | PASS   |
| TC-02 | Create booking with valid data        | 200 + booking ID      | 200 + booking ID       | PASS   |
| TC-03 | Get created booking                   | 200 + correct data    | 200 + correct data     | PASS   |
| TC-04 | Update existing booking               | 200 + updated data    | 200 + updated data     | PASS   |
| TC-05 | Verify updated booking                | Updated data persists | Updated data persisted | PASS   |
| TC-06 | Delete existing booking               | 201                   | 201                    | PASS   |
| TC-07 | Get deleted booking                   | 404                   | 404                    | PASS   |
| TC-08 | Login with invalid credentials        | Bad credentials       | Bad credentials        | PASS   |
| TC-09 | Get non-existing booking              | 404                   | 404                    | PASS   |
| TC-10 | Update without authentication         | 403                   | 403                    | PASS   |
