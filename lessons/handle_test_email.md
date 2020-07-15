---
title: Avoid test email being sent to actual users
permalink: handle_test_email.html
last_updated: Jul 14, 2020
folder: testing
---

### Context

In PROJECTX, since we had PH employee data (employees' email and their managers' email addresses), sending out test email notifications to actual users was not unlikely. This could be disruptive esp if the recipients are not directly involved in the testing of the project.

#### Similar cases

* Peter receiving test email notifications.

* Test email used was a bit too common (or very likely to be real e.g., `john@gmail.com`)

### Solutions

(1) Email addresses were modified so that they didn't use the `@domain.com`. However, a risk there is that if the substitute domain actually exists.

(2) The email notification system was updated to allow for the emails to be directed to a test email.  If a parameter was set, the email will be sent to a set of specified recipients rather than to the actual users.
