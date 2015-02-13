We've started using a consistant numbering system to mark all the ingots in are cargo deliveries, and everythign ahas worked nicely. Except for this morning. Our reporting systems have crashed and we need to find a way to fix them.

Ingots in each consignment are numbered in the row from A1 to Z9 as
A1, A2,..., A9, B1, B2, ..., Z9. Each consignment is marked with the number of the last ingot in it.
So you can define the quantity of ingots by the number of marks.

Our daily report is broken. For some reason all of the commas separating values were removed or replaced with a junk data.
We need to figure out which are the good marks in todays report. Each mark will look a little like "LD", where
"L" is a capital english letter and "D" is a digit ranging from 1 to 9 (zero indicates junk data).

You are given a report as a chunk of text. Your code needs to find all consignment marks and count the total quantity of ingots.
Take the report "ASDA1,BB22D01C1" for example. Here we can find three marks: A1, B2 and C1, so the result is 31.


This is a code golf mission and you code should be as short as possible.
The shorter code, the more points you can earn.
The smallest code length is 200 symbols.

**Input:** A broken report as a string.

**Output:** The total quantity of ingots as an integer.

**Example:**

```python
golf("ASDA1,BB22D01C1") == 31
```
**How it is used:**

Code golf missions help you to learn special tricks and give you a deeper understanding python as a language.

**Precondition:**

```python
all(ch in (string.ascii_letters + "123456789" + ",") for ch in report)
```

