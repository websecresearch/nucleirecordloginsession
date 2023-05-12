# nucleirecordloginsession

Nuclei template to record a login session for a web applications based on session cookies, jwt token.

This is a Nuclei template named "Record Authentication Session" which is used to record an authentication session for a web application that uses cookie, session, or JWT token-based authentication. The template has the following properties:

    id: A unique identifier for the template.
    info: General information about the template, including its name, author, severity, description, and optional reference links.
    tags: A list of tags that describe the template, including "login", "record", "session", and "authentication".
    requests: A list of requests that Nuclei will send to the web application to authenticate and record the session.

The template has three requests:

    A POST request to the /login endpoint, which sends a login request to the web application using the contents of a file named login_request.txt. The template includes a matcher to ensure that the login was successful, and two response templates to extract the authentication token and session cookie from the response.
    A POST request to the /auth/token endpoint, which sends a request to authenticate using a token. The contents of the request are stored in a file named token_request.txt. The template includes a matcher to ensure that the authentication was successful, and a response template to extract the authentication token from the response.
    A GET request to the root endpoint (/), which includes the authentication token and session cookie in the request headers. The template includes a response template to ensure that the response contains the word "Dashboard" in the title.

Overall, this template can be used to authenticate and record a session for a web application that uses various authentication methods, including cookie, session, JWT token.
