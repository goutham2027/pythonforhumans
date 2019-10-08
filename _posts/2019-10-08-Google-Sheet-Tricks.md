---
title: Google Sheets Tricks
tags: general
---

### Lock the formula of a cell.
Let's take an example, you are tracking your expenses (A: Date, B:
Expense Amount) in a Google Sheet
in reverse chronological order i.e. latest on the top and you have a
formula in some other cell where you compute sum from B2 (SUM(B2:B).


Every time you want to add a new entry, you add a row either from above or
below your references to the formula get updated. To avoid this from
happening using `INDIRECT` function. So your formula to compute sum
becomes `SUM(INDIRECT("B2:B"))`
