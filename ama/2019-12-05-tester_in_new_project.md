---
layout: post
title: How do testers prepare in a greenfield project that just started?
date: 2019-12-05 23:00:00 +0800
categories: [testing, agile]
tags: [project start]
---

### Question

Background: The project is for creating a new web/mobile application from scratch. The project had just started, and even the devs have not yet started coding. The tester is helping out with some of the requirements like doing an inventory of the screens and exploring reference application(s).

The tester asks: Can I start writing down test scenarios and test cases, and then collaborate with the BA for preparing the user stories for the coming sprint? Anything else that I can help with, at this point, that would be beneficial for the team?

### Answer

For the first question, if the user story is not yet groomed, it might be risky (in the sense of potential for rework) to create formal test cases for it because there's a possibility that the user story might be split or merged or modified further.

But definitely, you can help out in trying to groom the user stories. You can already outline the test scenarios or gather test ideas. That could also help reveal if the user story needs to be broken down further.

**Grooming user stories.**  Ideally, we have everyone in the team who'll work on the user story involved in the grooming. In some projects though, they happen to have dedicated BAs who are expected to be focused and responsible for it. But still, testers are in a good position to help flesh out the user stories because you'll be the ones to test and you'll need to know the criteria for you to be able to say the user story would pass testing and be ready for the PO to review.

**Modeling user stories** (as part of grooming). Modelling can help provide a different visual perspective of the scenarios or cases that you'll need to consider. As you model, you may also find gaps in the design or cases that need to be supported by the user story. This could be in the form of diagrams or tables, whichever would best fit your needs.

**Reviewing the designs** (somewhat still related to grooming). Like for the case of screen mock-ups or prototypes, you can give feedback if you think there are screen components that are off or were missed, or if you have usability suggestions. If there are DB designs, you can also check the tables and fields to see if they capture the entities and attributes that will be used by the application. Although this might overlap with the BA's work, so just align with the BA on how much work you'll offer.

**Other prep work for testers who just joined a really, really new project**

**Testing research.** For example, if you'll be working with a certain technology (e.g., PWA, SQL), and especially if you're still unfamiliar, this would be a good time to research on the topic. You can look for what could be the possible risks, or usual bugs, or tips or techniques on testing this.

**Test tools** (as part of research). Especially for a new project, you need to familiarize yourself with the available tools that had been prescribed. Or sometimes, you'll have to look for new testing tools. Say, how will you manage test cases, or bugs. Or if you need access to the database, what DB client would you need to use. Or if you need emulators.

**Testing process.** The test lead usually is the one who helps identify the scope of the work of the test team. For Agile, by default, testers will pretty much need to test the implemented features or user stories. If there's going to be a documentation of test cases, then need to consider what would be the test case review process. Or what would be the exclusions or inclusions. Like for a previous project, initially we were creating test cases for all user stories. Then as we went along, we agreed on having test cases prepared only for those with story points 5 and above.

**Standards or guidelines.** Especially for big teams, conventions for test cases and bug reports would be helpful so that there is some semblance of organization when folks look into the repository. Esp if they have to report progress or status. Another aspect is that having standard test cases, or at least reminders/guidelines, can be helpful in keeping folks aware of frequently missed bugs. Like in a previous team, we had a standard test plan wherein we refer to for checking components that are spread across functions. For instance, we had to check that the page title has a particular format, and those kinds of details aren't usually enumerated as acceptance criteria of user stories but are nevertheless checked for.
