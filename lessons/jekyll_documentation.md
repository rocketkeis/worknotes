---
title: Documentation using Jekyll
permalink: jekyll_documentation.html
last_updated: Jul 13, 2020
folder: misc
---

### Context

Looking for documentation options with the following considerations:

* Available within the company
* No extra cost to the team for infra or subscription
* Low maintenance

### Why this approach (using Jekyll and GitHub)?

* I've seen several sites that make use of this, aside from my personal notes.
* Lightweight - content are just in Markdown files
* Free - No need to pay for licenses to use this approach. I don't have to worry about infra, or if an app goes down. And if GitHub or Ruby goes out of commission, I think there would be bigger problems than this documentation.
* Focus can be on the content rather than on the tool housing the content.
* Setup and content management can be achieved with little to no coding background.
* Also this is being somewhat promoted in the company. Some global groups are using this approach (or MkDocs instead of Jekyll, but essentially inner sourcing).

### Why not the other tools like SharePoint, etc.?

Below are some of the options available within the company, and sharing below why I didn't go for them.

* [SharePoint](#sharepoint)
* [Confluence](#confluence)
* [OneNote](#onenote)
* [MS Teams Wiki](#ms-teams-wiki)

#### SharePoint

This is probably the most widely used within the org. It's readily available to us. It's easy to get one created, you just have to submit a form, no approvals needed. Maintaining the site is mostly straightforward, WYSIWYG, and you'd get by with no coding know-how involved. Access can be controlled so that only the persons you want to have access actually get access. You have options to use pages, a document library, or a wiki.

What I don't like:

* A general pet peeve of mine is when I click on a link and it turns out to go to a page with a link to a file that I then have to download, and then downloading and opening it only to find that it's only got a few lines of useful text (and worse just placeholder text). You could have showed me the useless text in the page in the first place, and spared me all the other steps. Of course, better if there's actually useful text.
* IDK how to update the site or its collaterals. Say, there's a typo or content that needs revising. There's no equivalent `CONTRIBUTING.md` on how improvements can be made. Usually what happens is you modify your local or own version, but the "bugs" you fixed will still be there in the site ready to be encountered by the next user.
* Coming from an org that used TWiki and then trying out SharePoint Wiki, the latter just didn't work for me. More on that [here (SharePoint vs TWiki)](https://twiki.org/cgi-bin/view/Codev/SharePointVsTWiki), if you're interested.

#### Confluence

I was able to use Confluence for a project before. It's a much better wiki than the SharePoint one. It seems to be setup for projects rather than organizations though. In the request form via GitHub issue, you need to specify your project and I'm not sure what their requirements are to be counted as a project.

What I don't like:

* Requesting access is done via GitHub issue. Not sufficient to just have Global Pass credentials. The admin has to create or activate accounts for them to have access. So for every member of the team, you'd have to make the request for the access to be granted. As opposed to SharePoint, that the admin can do it themselves.
* Not clear what the requirements are to be counted as a project. I tried to request a project space before and I was told that they couldn't find the project I was requesting for, which gave me the impression that there's an official list of projects that they check against.

#### OneNote

Just gets so disorderly overtime as more and more content gets added. Perhaps it's because adding of content is too freely accessible.

What I don't like:

* Can easily get unwieldy and just messy. Maybe it's a better fit for personal notes than for team documentation.
* Can sometimes have sync problems (or maybe I'm just unlucky)

#### MS Teams Wiki

Pretty much the same sentiment as with OneNote on how it can just get messy. I feel like it's an option for a working space for an item for quick discussion or note-taking. But afterwards when something more conclusive is already drafted, you'd want to transfer it out of there.

What I don't like:

* Can easily get unwieldy and messy
* Can't do anchors to link to a particular section of the wiki
* No version history, can't see who changed what and when
* Plus what he said: ["Don't use Teams wiki"](https://myteamsday.com/2018/05/08/dont-use-teams-wiki/). Post was written in 2018, but as the author commented it still holds this 2020.
