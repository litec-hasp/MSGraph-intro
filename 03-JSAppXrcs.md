# JavaScript App for MS 365 Data

Based on [MS Training - JS Graph App](https://learn.microsoft.com/en-us/training/modules/msgraph-javascript-app/).

---

## Objectives

- Understand the role of Azure AD (Active Directory) with MS Graph
- Understand MS Graph permissions
- Registering an Azure AD application
- Create a JavaScript app to connect to MS Graph and retrieve Microsoft 365 data

---

## Microsoft Identity Platform

> See [MS Training - Identity Platform](https://learn.microsoft.com/en-us/training/modules/msgraph-javascript-app/2-azure-ad-graph)

- Helps to deal with
  - authentication
  - authorization
  - SSO (single sign on)
  - security tokens
  - ...
- Provides SDKs / libraries for various programming languages
  - Example MSAL (Microsoft Authentication Library)

- Key Part of the identity platform is Azure AD

---

## MS Graph Permissions

> See [MS Training - Graph Permissions](https://learn.microsoft.com/en-us/training/modules/msgraph-javascript-app/2-azure-ad-graph)

- **Scope**:
  - resources access (user / mail / groups / ... )
  - allowed operations (read / write / ...)
- **Permission types**:
  - *delegated* -  Graph call on behalf of the user
  - *application* - for background processes / automation
- **Access Tokens**:
  - received after permission request and admin consent
  - for authentication and authorization
  - passed in the authorization header of each HTTP request<br>
    with the word "Bearer" and a space before it

### Example Authorization Header

```rest
GET https://graph.microsoft.com/v1.0/me/ HTTP/1.1
Host: graph.microsoft.com
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
```

---

## Application Registration - Azure AD

> See [MS Training - App Registration](https://learn.microsoft.com/en-us/training/modules/msgraph-javascript-app/4-register-application)

- **To connect your application to MS Identity, you need to register your app in Azure AD.**

- Azure AD provides app registration for:
  - web
  - single-page
  - mobile
  - desktop applications
  
  that can be accessed through the Azure portal or through the Azure CLI.

- It provides you with unique information to retrieve an access token:
  - application ID
  - tenant ID

### Exercise

See [MS Training - Register App](https://learn.microsoft.com/en-us/training/modules/msgraph-javascript-app/5-exercise-register-application)

---

## Access Token Retrieval

> See [MS Training - Access Token Retrieval](https://learn.microsoft.com/en-us/training/modules/msgraph-javascript-app/6-retrieve-access-token) and [MS Training - Token with MSAL](https://learn.microsoft.com/en-us/training/modules/msgraph-javascript-app/7-exercise-retrieve-access-token).
