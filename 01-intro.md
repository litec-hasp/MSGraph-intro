# MS Graph

## Introduction

---

## What is MS Graph?

> MS Graph is a secured, unified API to connect to data located in various Microsoft 365 services.

- Just one API for different services
- Main focus on developers
- MS Graph REST API
- Powershell implementation exists

> :warning: It is NOT GraphQL or a graph based database!

---

## What Kind of Data can be Accessed?

> Access to Azure / Active Directory / O365 / ...

- Users and groups

- Teams data
- Tasks
- Files
- Mail
- Meetings and calendars
- Organizational charts

<img src="https://learn.microsoft.com/en-us/training/m365-developer/msgraph-intro-overview/media/2-microsoft-graph.png" style="zoom:42%;margin-left:40px" />

<small>Image Source: <https://learn.microsoft.com> </small>

---

## MS Graph Services

- Centered on
  - Users
  - Groups
- Support scenarios related to
  - identity
  - security
  - productivity
  - collaboration
  - ...

---

## Using MS Graph services

### MS Graph REST API

Example - User Profile Call:

```sql
GET /users/<name>@<tenant>.onmicrosoft.com
```

This will return a JSON Representation of the user profile.

### MS Graph SDK and Client Libraries

- For different programming languages, like
  - C#
  - Java
  - Java Script / Type Script / Node.js
  - PowerShell
  - ...

-----

# Microsoft Graph Explorer

> :link: <https://developer.microsoft.com/graph/graph-explorer>

- web application
- free, open-source tool
- allows Graph REST API requests
- for testing, prototyping

---

## Exercises <small>1/2</small>

1. Visit [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer) and try some queries with the demo account.

2. Log in with your developer account.
   - you should have setup an demo tenant<br>
     (E5 Subscription) in you ms dev account
   - use your Microsoft 365 developer tenant
   - login with your admin user
   - set consents for app

3. Try **"GET my profile"** Sample Query
   - **request:**
     - try out the different tabs - especially `Modify Permissions`
     - atm we just have `User.Read` Permission - we only can view our own profile
   - **response:**
     - JSON with name / job / mail / id / ...
     - try out the different tabs

---

## Exercises <small>2/2</small>

4. Try **"GET my mails"** Sample Query
   - response gives access denied
   - switch to: `Request -> Modify Permissions`
   - Click on `Mail.Read` Consent
   - try query again - now you should see your mail(s) as JSON

5. Now it is time to solve your *FIRST ASSIGNMENT* :scream:

   > **Find a channel in one of the teams you are member of, and
   write "HELLO WORLD!" (or any other text) into that channel.**

   - *TIP* - Have a look at the MS Teams Sample Queries
     - use them to find out your teams and channels
     - add some Consents
     - use a POST-query to write data

6. Have a look at MS Teams (dev account), and find out if your message arrived

7. Be proud of yourself! :tada:

---

## Graph Explorer Code Snippets

> You want to write code for your app?<br> Not just some tryouts in a browser?<br>
> **Fear not! The solution is already there!**

- Have a look at the "Code Snippets"-Tab within the response field
- You will find code for C# / JavaScript / Java / Go / Powershell
- Don't forget to copy the "Access Token" (see according tab in request field)
  - The programming languages authentication steps vary!
- Use at your own risk!
