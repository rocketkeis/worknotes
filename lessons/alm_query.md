---
title: ALM Query
permalink: alm_query.html
last_updated: Jul 13, 2020
folder: testing
---

### Context

Test cases and test steps had already been uploaded and updated in ALM (v?). What's needed is to be able to extract the test cases and test steps into an excel file so that these can be reuploaded again.

### Solution

1. Download and install the connectivity tool from ALM Tools.
2. In Dashboard > Analysis view, add a New Excel Report.
3. Using the Query Builder, figure out the query you can use.
4. Generate the report.

### Query: Test cases and test steps under a folder

You’ll need to search ALL_LISTS for the corresponding folder so that you can specify the correct one in the WHERE condition. It doesn’t preserve the folder tree structure though.

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
