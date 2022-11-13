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

## Uisng MS Graph services
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
