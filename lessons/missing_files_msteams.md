---
title: Missing MS Teams files
permalink: missing_files_msteams.html
last_updated: Aug 6, 2020
folder: misc
---

### Context

A team was using MS Teams for their file repository. It was then discovered that the files in a certain channel had gone missing.

### Root Cause

This was traced to sync issues. It's possible that a member's local is linked or hooked to be synced with the Team folder. Deleting in the local would cause the files to be deleted in the team repository as well when it gets synched -- which is as designed.

### Solution

* Upon discovering the files are lost or at risk of being lost, communicate with the rest of the team so that they can also check if their files had been missing.
* For MS Teams, it uses SharePoint and SharePoint has a Recycle Bin folder so restoration is feasible. Unless the Recycle Bin has been emptied then the files are lost.

### Other Suggestions

* Last resort would have been to reach out to team members for locally stored copies of lost files.
* Employ quarterly back up of files as another backup option.
* Disseminate known best practices or watch-outs on MS Teams file management to the rest of the team.
