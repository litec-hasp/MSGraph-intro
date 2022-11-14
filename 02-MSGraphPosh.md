# MS Graph & PowerShell

Based on [MS Training - Introduction to Microsoft Graph PowerShell](https://learn.microsoft.com/en-us/training/modules/introduction-to-microsoft-graph-powershell/)<br> and [MS Training - Manage Windows updates for cloud-connected devices by using the Microsoft Graph PowerShell SDK](https://learn.microsoft.com/en-us/training/modules/manage-windows-updates-cloud-devices/).

---

## Objectives

- Understanding of MS Graph PowerShell SDK

- Overview on types of processes that MS Graph PowerShell can automate

- Application scenarios on Azure AD and MS 365
  - Adding new users
  - removing access from previous users
  - update user info
  - reset passwords
  - manage access to resources by assigning roles to users
  - ...

---

## What is Microsoft Graph PowerShell?

- SDK (Software Development Kit) for access to MS Graph REST API
- Acts As API wrapper for REST queries
- PowerShell (meta)-module - `Microsoft.Graph`
  - Container for other modules
- Core module - `Microsoft.Graph.Authentication`
  - SignIn - `Connect-MgGraph`
  - Rest queries via: `Invoke-MgGraphRequest`
  - Switch version (v1.0 and beta)
  - Permissions

---

## Command Structure

```powershell
{Verb}-Mg{Resource}
```

- `Verb` ... typical PS Verbs (Add, Clear, Copy, Get, Set, New, Remove, ...)
- `Mg` ... Microsft Graph
- `Resource` ... Graph resources (User, Group, Team, Mail, ...)

---

## MS Graph Powershell - Features

- Access to all Microsoft Graph APIs (single endpoint and access token):
  - Azure AD,
  - SharePoint,
  - Exchange,
  - Outlook, ...
- PowerShell 5.1 and 7 (cross platform)
- Authentication via Microsoft Authentication Library (MSAL)
- Least privilege:
  - permissions are NOT pre-authorized
  - users must perform one-time request for different app permissions
- "Advanced queries" via eventual consistency (?)
- Open source
- Regular updates

---

## Installation

> :warning: Installing the main module will install all the 38 sub modules. Consider to install only necessary modules!

- Recommended to use PowerShell 7, but 5.1 works too
- Detailed Information: [Learn MS - Install Graph PoSh](https://learn.microsoft.com/en-us/powershell/microsoftgraph/installation?view=graph-powershell-1.0)
  - Execution Policy
  - Install / Update / Uninstall

```powershell
# list modules for individual installation
Find-Module Microsoft.Graph*

# install a specific module
Install-Module Microsoft.Graph.Groups 

# install all modules ("globally" on device)
Install-Module Microsoft.Graph

# install all modules (for current user)
Install-Module Microsoft.Graph -Scope CurrentUser
```

---

## `Connect-MgGraph` - Sign In

- Two types of authentication:
  - delegated (user)
  - app-only access (requires admin consent)
- Optional `Scopes` parameter is used to get consent
  - only needed once (consent is stored)

```powershell
# Info about Graph connection command - extra parameters!
Get-Help Connect-MgGraph

# connect and get consent for user read all
Connect-MgGraph -Scopes "User.Read.All"

# disconnect
Disconnect-MgGraph
```

---

## Selection of Commands

See [MS Training Graph PS Intro](https://learn.microsoft.com/en-us/training/modules/introduction-to-microsoft-graph-powershell/3-how-microsoft-graph-powershell-works)...
