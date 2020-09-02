---
title: Missing MS Teams files due to renamed channels
permalink: missing_files_msteams2.html
last_updated: Aug 18, 2020
folder: misc
---

### Context

A team was using MS Teams for their file repository. It was then discovered that the files in a certain channel had gone missing.

### Lesson Learned

* Name channels right, the first time (if possible)
* If renaming channels, don't rename corresponding SP folder.

[From Microsoft](https://blogs.perficient.com/2020/02/02/the-pains-of-renaming-channels-in-teams-2/)

> I hope you’ve all learned an important lesson today. Either leave your SharePoint folder name as the original name or create a new channel and copy over your files to the new channel. If Microsoft changes this capability in the future where a change to the channel name in Teams syncs with the associated SharePoint folder then I’ll be sure to update this blog, but I wouldn’t hold your breath, they’ve been “[working on it](https://microsoftteams.uservoice.com/forums/555103-public/suggestions/16934143-rename-of-team-channel-doesn-t-rename-associated-s)” for three years now ;).

### Root Cause

Missing files were traced to an adverse impact of renaming a channel.

* When MS Teams channels are created, they get corresponding folders in the SharePoint.
* After renaming the channel in MS Teams, the folder in SharePoint still had the original name.
* Stabilized/worked for a bit until someone uploaded a file into the folder from Windows Explorer (via synched folder)
* MS Teams created a new folder in SP with the _original name_ therefore showing files folder as "blank". Folder with _renamed name_ is still in SP with all of the files.

### Solution

* Copied over files from _RENAMED NAME_ to _ORIGINAL NAME_; renamed _NEW NAME_ to _RENAMED NAME OLD_
* Moved _RENAMED NAME OLD_ to a back-up folder in SP


### Action Needed (if you have locally synchronized this folder)

Please unlink/stop synching this folder and resync:

* Stop sync in OneDrive
* Safely delete folder in Windows Explorer
* Re-sync from MS Teams
