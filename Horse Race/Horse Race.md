# Horse Race

## Problem

**There are 25 horses, each of which runs at a constant speed different from the others. The race track has 5 lanes, so at most 5 horses can race at a time. What is the minimum number of races needed to determine the 3 fastest horses?**

<details>
<summary>Click to see the solution</summary>

### Solution

This problem tests basic analytical reasoning. To find the 3 fastest horses, all horses need to be tested. Here's the step-by-step process:

#### Step 1: Divide the horses into groups of 5 and race them
- Divide the 25 horses into 5 groups:  
  - Group 1: Horses 1–5  
  - Group 2: Horses 6–10  
  - Group 3: Horses 11–15  
  - Group 4: Horses 16–20  
  - Group 5: Horses 21–25  

- Run 5 races, one for each group, and record the order of the horses within each group.  
  For example, assume the order is as follows:  
  - Group 1: `1 > 2 > 3 > 4 > 5`  
  - Group 2: `6 > 7 > 8 > 9 > 10`  
  - Group 3: `11 > 12 > 13 > 14 > 15`  
  - Group 4: `16 > 17 > 18 > 19 > 20`  
  - Group 5: `21 > 22 > 23 > 24 > 25`

#### Step 2: Race the fastest horses from each group
- Race the top horses from each group: `1, 6, 11, 16, 21`.  
  Suppose the result of this race is:  
  `1 > 6 > 11 > 16 > 21`.

#### Step 3: Eliminate impossible candidates
- From the results of Step 2, we can eliminate horses that cannot possibly be in the top 3:
  - Horses in Groups 4 and 5 (e.g., `16–20` and `21–25`) are eliminated because the fastest horse from each group ranked 4th or 5th overall.
  - Within each group, only the top 3 horses need to be considered further.

#### Step 4: Determine the top 3 horses
- The remaining candidates are:  
  - From Group 1: `1, 2, 3`  
  - From Group 2: `6, 7`  
  - From Group 3: `11`

- Run one final race with these horses: `2, 3, 6, 7, 11`.  
  The top 2 horses in this race, along with `1` (the overall fastest horse from Step 2), are the top 3 horses.

#### Final Answer:
- **Minimum number of races:** **7** (5 initial races + 1 race for group leaders + 1 final race for top 3 determination).

</details>