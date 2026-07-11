---
title: "Week 11 Worklog"
date: 2026-07-05
weight: 2
chapter: false
pre: " <b> 1.11. </b> "
---

{{% notice warning %}}
⚠️ **Note:** The information below is for reference purposes only. Please **do not copy it verbatim** into your report, including this warning.
{{% /notice %}}

### Week 11 Objectives:

* Add tests for JWT authentication and the user login flow.
* Build a GPS distance checking service for anti-fraud validation.
* Complete anti-fraud configuration, test helpers, and CI automation for database migrations and tests.

### Tasks to be completed this week:

| Day | Tasks | Start Date | Completion Date | Reference Materials |
| --- | --- | --- | --- | --- |
| 2 | - Write unit tests for **CognitoIdentityProvider** to verify JWT authentication scenarios.<br>- Create a helper to generate JWTs using an in-memory RSA key pair so tests do not need to connect to Cognito.<br>- Validate valid tokens, invalid tokens, and incorrect authentication data. | 06/07/2026 | 06/07/2026 | <https://cloudjourney.awsstudygroup.com/> <br> <https://www.youtube.com/@AWSStudyGroup/videos> |
| 3 | - Write integration tests for the Express login feature.<br>- Test the flow for retrieving user information after login.<br>- Use the **trusted-local header** to mock users in the test environment. | 07/07/2026 | 07/07/2026 | <https://cloudjourney.awsstudygroup.com/> <br> <https://www.youtube.com/@AWSStudyGroup/videos> |
| 4 | - Add integration tests for valid users, **SUSPENDED** accounts, and requests without a token.<br>- Improve the test helper to create test data more conveniently and flexibly.<br>- Ensure test data can be reused across multiple testing scenarios. | 08/07/2026 | 08/07/2026 | <https://cloudjourney.awsstudygroup.com/> <br> <https://www.youtube.com/@AWSStudyGroup/videos> |
| 5 | - Build a GPS distance service using the **Haversine** formula.<br>- Return the distance between the user and the restaurant, and check whether the distance is within the allowed threshold.<br>- Create the **antiFraud.js** configuration file to manage anti-fraud parameters and allow the GPS distance threshold to be configured through environment variables. | 09/07/2026 | 09/07/2026 | <https://cloudjourney.awsstudygroup.com/> <br> <https://www.youtube.com/@AWSStudyGroup/videos> |
| 6 | - Add input validation for the GPS service.<br>- Write unit tests for the GPS service covering zero distance, within threshold, outside threshold, exactly at threshold, and invalid input data.<br>- Update GitHub Actions to automatically run database migrations and the Vitest test suite; run all unit tests successfully. | 10/07/2026 | 10/07/2026 | <https://cloudjourney.awsstudygroup.com/> <br> <https://www.youtube.com/@AWSStudyGroup/videos> |

### Week 11 Achievements:

* Completed unit tests for **CognitoIdentityProvider**, covering key JWT authentication scenarios and using an in-memory RSA-based JWT generation helper.

* Completed integration tests for Express login and user profile retrieval, including valid users, **SUSPENDED** accounts, and requests without a token.

* Successfully built a GPS service using the **Haversine** formula to calculate the distance between users and restaurants and validate it against the allowed threshold.

* Created the **antiFraud.js** configuration file to manage anti-fraud parameters and support GPS distance threshold configuration through environment variables.

* Added unit tests for the GPS service with multiple scenarios and invalid input validation.

* Updated GitHub Actions to automatically run database migrations and the Vitest test suite, and improved the test helper to make test data creation more convenient.
