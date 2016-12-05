---
title: "FYI"
bg: orange
color: black
fa-icon: warning
---

## Key notes
<a name="destructive" />

* IPSOS contains only treated patients. 
    + Information is not collected on patients recieving surgery, radiotherapy or supportive/watchful waiting etc.
* Batches are stacked
    + Batches contain all previous data
    + Projection factors from previous years are often tweaked - so use the latest data only!
* Projection factors
    + Later lines are oversampled and sometimes companies pay for oversampling on other variables as *supplements*
    + Oversampling means you cannot use the raw percentages!
    + Projection factors represent the weighting of that patient toward the year (year being defined by `dat_process`, not `dat_consult`
    + `projvalp` is based on that individual's weight towards the total for that tumor site in that year
    + `projval` is recomended, as it's the treatment oppurtunities per year
* Doses
    + Note that the daily dose needs to modified to represent a cycle dose
