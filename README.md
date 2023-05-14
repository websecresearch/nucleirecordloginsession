# nucleirecordloginsession

Description:
This template is used to record the login process for any web application and reuse the session for subsequent requests. It also follows redirection and performs matchers to validate the response.

Author:
This template was created by websecresearch.

Severity:
The severity of this template is set to info.

Requests:
The template contains a single request consisting of two parts. The first part is a GET request that retrieves the login page. The second part is a POST request that sends the credentials to the login page and logs the user in. The credentials are taken from a file specified in the Content-Type header.

The requests also contain the following options:

    redirects: true: This option is set to follow any redirects that occur during the login process.
    cookie-reuse: true: This option is set to reuse the session cookie to maintain the session across subsequent requests.
    req-condition: true: This option is set to ensure that the request is sent only if the conditions specified in the matchers are met.

Matchers:
The template contains a single matcher that validates the response. The matcher is of type dsl and checks if the response body contains the string "Hello Admin User". If the response matches this condition, the request is considered successful.

Overall, this template can be used to automate the login process for any web application that requires credentials to be entered. It is flexible enough to accommodate different login forms and can be easily customized to fit specific use cases.
