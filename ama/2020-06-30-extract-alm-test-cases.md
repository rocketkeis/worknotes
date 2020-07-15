---
layout: post
title: How to extract the test cases and steps from ALM?
date: 2020-06-30 12:25:00 +0800
categories: [testing]
tags: [alm]
---

### Question

How can you extract the test cases and steps from ALM?

### Method 1 (Excel format)

1. Download and install the connectivity tool from ALM Tools. (The link to this is just within ALM)
2. In Dashboard \> Analysis view, add a New Excel Report.
3. Using the Query Builder, specify the query (the one I used is shared below).
4. Generate the report.

For this query, you'll need search in `ALL_LISTS` to find the corresponding folder to specify in your `WHERE` condition. The downside though is this doesn't preserve the folder tree structure as you see it in ALM. It just lists per test cases and steps according to folder.

```
SELECT
  TEST.TS_SUBJECT,
  ALL_LISTS.AL_DESCRIPTION as "Folder Name",
  TEST.TS_TEST_ID as "Test ID",
  TEST.TS_NAME as "Test Name",
  TEST.TS_DESCRIPTION as "Test Description",
  DESSTEPS.DS_STEP_ORDER as "Step Order",
  DESSTEPS.DS_STEP_NAME as "Step Name",
  DESSTEPS.DS_DESCRIPTION as "Step Description",
  DESSTEPS.DS_EXPECTED as "Expected Results",
  TEST.TS_RESPONSIBLE as "Designer"
FROM TEST
  JOIN ALL_LISTS on TEST.TS_SUBJECT = ALL_LISTS.AL_ITEM_ID
  JOIN DESSTEPS on TEST.TS_TEST_ID=DESSTEPS.DS_TEST_ID
WHERE All_LISTS.AL_ABSOLUTE_PATH like'AAAAAPAAGBCIAAAAAAAAAAAC%'
ORDER BY TEST.TS_SUBJECT, TEST.TS_TEST_ID, DESSTEPS.DS_STEP_ORDER
```

### Method 2 (Docx, HTML, PDF format)

1. In Testing \> Test Plan, find the folder that you'd like to work with.
2. Select the folder.
3. From the menu, click on Analysis \> Project Report \> Tests with Design Steps.
4. A preview is going to be generated. Click on Add to Analysis Tree, and just follow along with the steps to save it.
5. You should automatically be taken to the Analysis view. If not, go to Dashboard \> Analysis view to find the newly created project report.
6. Generate the report.

### Method 3 (Excel format)

Another option requires scripting a macro in Excel. The macro file we got didn't work though. So in case anyone has a working copy, please share the script or the excel file (unprotected so we can check under the hood).
