# Industrial App Store Release Notes

This page describes the release notes for the [Industrial App
Store](https://appstore.intelligentplant.com) portal.

### 2020-05

This release contains the following changes:

  - Secret Key validation when using PKCE flow.
  - App Store Custom Error Pages.
  - Minor fixes for the new app publishing process.
  - Functionality to remove app profile media.

### 2020-04

This release contains the following changes:

  - You are no longer required to log in to browse the available apps in
    the Industrial App Store.
  - We have fixed an issue that could sometimes prevent JavaScript
    applications from successfully signing in when using the OAuth2
    authorisation code flow.
  - We have fixed an issue that prevented JavaScript applications from
    being able to query the user info API endpoint.
  - We have fixed some issues related to updating app settings,
    including editing or cropping the icon and banner image for an app.

### 2020-03

This release contains the following changes:

  - A bug that prevented organisation users from being removed from
    groups has been fixed.
  - We have refreshed the app settings page for app developers.
  - [PKCE support](https://oauth.net/2/pkce/) has been added for public
    apps that were previously using the [OAuth 2.0 implicit
    flow](https://oauth.net/2/grant-types/implicit/). Implicit flow is
    still available, but app developers must now explicitly enable it if
    it is required by an app.
  - Secret keys for apps are no longer visible in the settings page.
    Now, the secret key is only displayed when it is initially created.
    You can reset the secret key for your app at any time.
  - You can pre-select all scopes required by your app from the app
    settings screen, and you can also pre-specify whether or not your
    app requests offline access (i.e. refresh tokens) by default. This
    simplifies the creation of the redirect URL your app uses when
    logging a user in. These options can still be specified in the
    redirect URL if preferred.
  - We've fixed a few other under-the-hood bugs.

### 2020-02

This release contains a high-priority fix related to changes in the way
Google Chrome handles cookies. The change affected the way organisation
users signed in using their Azure Active Directory credentials.
