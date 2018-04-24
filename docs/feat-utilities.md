---
id: feat-utilities
title: Utility Methods
---
**************************************************************************************************
Table of Contents
- [Renew Security Token](#renew-security-token)
  - [Syntax](#syntax)
  - [Description](#description)
- [Get Library Version](#get-library-version)
  - [Syntax](#syntax1)
  - [Description](#description1)
  - [Description](#example)
**************************************************************************************************

## Renew Security Token

### Syntax
`sprLib.renewSecurityToken()`

### Description
Refreshes the SharePoint page security digest token.  

Starting in SP2013, `.aspx` pages include a security digest token in a hidden input element that will expire
after 30 minutes (by default).

This method allows the refresh of this value, which can be useful in certain cases.  An example would
be an application that provides a tool-like interface (e.g.: List Mass Updater) where the page token could
expire before all operations have completed.

NOTE: SpRestLib will refresh the token automatically as needed during CRUD operations.

## Get Library Version

### Syntax
`sprLib.version`  
`sprLib.ui.version`

### Description
Returns the version and build for the library currently loaded.

### Example
```javascript
sprLib.version
"1.4.0-20180101"

sprLib.ui.version
"1.0.0-20180202"
```