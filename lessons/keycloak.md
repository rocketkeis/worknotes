---
title: Keycloak to simulate official IDM
permalink: keycloak.html
last_updated: Jul 13, 2020
folder: misc
---

### Context

PROJECTX uses the organization's official IDM (Identity Management) tool for user authentication. However, they only provide at most 5 test users in the non-production environment. This won't be enough to test different personas, or cases involving different users and roles.

### Solution

[Keycloak](https://www.keycloak.org/)

* open source; and like the official IDM, it is used for identity and access management.
* in theory, you put why this solution fits here.

### Other options

* Initially, we created dummy registration and login functionalities. But downside are:
    * we need to be mindful of not deploying these changes onto production.
    * not a simulation of the official IDM.
