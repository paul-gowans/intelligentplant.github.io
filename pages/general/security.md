# App Store Security

The App Store is a platform where users purchase and spend credits, and
apps perform sensitive data operations. Therefore, security is
paramount.

We aim for the highest web security standards. Here's an overview of our
policies.

## Secure Web Requests and HTTPS

    Can information you send and request be intercepted over the internet?

Take a look at the address bar in your web browser.

![](/general/https.png)

Note the padlock and "https" prefix in our web address.

*HTTP* stands for Hyper Text Transfer Protocol, the communication
protocol of the World Wide Web. *S* stands for secure. It means **all
communication between you and the App Store is encrypted**. It is the
same approach used in banking websites.

Encryption does not prevent message interception, but it does mean the
information content is secure.

-----

## Logging in to the App Store and User Authentication

    Is a user who they claim to be?

Any interaction between a user and the App Store must be authenticated.
If a user is not authenticated, App Store redirects to a log-in page.

We provide two main methods for user authentication:

### 1\. Log in with your Social Media (LinkedIn or Google) account

Using a social media site as an authentication provider is an
increasingly popular method of managing the log-in process. It means you
don't need to set-up and remember a dedicated log-in for the App Store,
and we can employ a trusted 3rd party security provider. At no point is
your LinkedIn or Google password divulged to us.

### 2\. Log in with your work account

An organization can register with the App Store to allow it's employees
to log in with their work accounts.

This is managed via Microsoft Azure Active Directory:

*"Azure AD can be integrated with an existing Windows Server Active
Directory, giving organizations the ability to leverage their existing
on-premises identity investments to manage access to cloud based SaaS
applications." *

[Microsoft Azure Active
Directory](https://azure.microsoft.com/en-us/documentation/articles/active-directory-whatis/)

-----

## Application Security

    Can I trust the Apps in the App Store?

The App Store is a marketplace of Industrial Applications from a variety
of vendors. However, all adhere to our security architecture which
forces applications to request explicit user authorization.

When you log in to an App Store app, you'll receive an authorization
prompt like the following:

![](/general/authorize.png)

  - An app can only access your App Store profile if ***you*** authorize
    it.
  - An app can only charge your App Store account if ***you*** authorize
    it.
  - An app can only access datasources ***you*** authorize it to access.

You can revoke this authorization at any time.
