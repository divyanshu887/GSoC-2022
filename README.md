
# GSoC 2022 Report: Social Street Smart

### *By Divyanshu Singh* 

[Download the Extension (Chrome Webstore)](<https://chrome.google.com/webstore/detail/social-street-smart/ddjcjpfkmcgpgpjhlmdenmionhbnpagm?hl=en-GB&authuser=0>)

[Chrome Extension Repository](https://gitlab.com/aossie/social-street-smart)

[All API's Repository](https://gitlab.com/aossie/social-street-smart-api)





#### Summary

This was the fourth year for Social Street Smart. Building upon the work done in the previous year, this year's GSoC tasks were aimed to safeguard users from Malicious URLs and improve their experience. 

Here is a quick summary of the work done over this year:

- :construction_worker: A CI / CD Pipeline has been added with
  - :white_check_mark: Unit Tests for all Newly Created APIs 
  - 🚀 Deployment through the GitLab Pipeline
- :sparkles: New Features -
	-  *Security Header Checker API*.
	-  *SSL Validator API*.
- :bento: Addition of a new front-end where ever needed
- :bug: Fixing bugs 
- :rocket: Deployed the Updated Chrome Extension to the Chrome Webstore.


#### Unit Testing [ For Newly Created Features ]

I have implemented Unit Testing into the project, that makes it much easier to validate that all the APIs are functioning properly. The tests run in GitLab's CI/CD Pipeline. Pytest was used to run the tests for the APIs.



#### Running the APIs locally

##### SSL Validator API

This can be run locally in the same way as they were before GSoC 2022. The steps are as follows

```bash
# Go to the directory of the API
cd /server/Security-Headers

# Install all the requirements
pip install -r requirements.txt

# Run the server
flask run
```
##### Security Header API

This can also be run locally in the same way as they were before GSoC 2022. The steps are as follows 

```bash
# Go to the directory of the API
cd /server/SSL

# Install all the requirements
pip install -r requirements.txt

# Run the server
flask run
```

For making the API calls, please follow the following format

```bash
For SSL Validator API
`localhost:5000/ssl/?urls=<LINK_FOR_LOOKUP>`

For Security Header API
`localhost:5000/shc/?urls=<LINK_FOR_LOOKUP>`
```

The API keys are to be encoded in base64 and passed as a string.

##### Unit Testing the APIs

Unit testing for the APIs was done using `pytest` . 
To run the tests locally

##### For SSL Validator and Security Headers API

```bash
cd /server/<directory_of_the_API>
pip install -r requirements.txt
pytest
```

#### Merge Requests

The following merge requests were made to the project during GSoC 2022.

##### Social Street Smart API Repository
- [!16 Combined PRs for SSL Validator and Security Header Checker API (Merged)](https://gitlab.com/aossie/social-street-smart-api/-/merge_requests/16)

##### Social Street Smart Repository (Chrome Extension)
- [!94 Added new UI for Settings Page (Merged)](https://gitlab.com/aossie/social-street-smart/-/merge_requests/94)
