# Trailing Zeros

## Problem

**How many trailing zeros are there in 100! (the factorial of 100)?**

<details>
<summary>Click to see the solution</summary>

### Solution

This is a straightforward problem. Trailing zeros in a factorial are created by multiplying pairs of **2 and 5**, as each pair produces a factor of 10.

In the factorial of 100 (**100!**), the frequency of **2** is much higher than the frequency of **5** in the prime factorization. Thus, the number of trailing zeros is determined by the frequency of **5** in the factorization.

#### Step-by-Step Explanation:
1. **Count the multiples of 5:**  
   Among the numbers from 1 to 100, the following are divisible by 5:  
   `5, 10, 15, 20, ..., 100`  
   There are **20 numbers** divisible by 5.

2. **Count additional multiples of 5² (25):**  
   Among these 20 numbers, some are divisible by **25**, contributing an extra factor of 5:  
   `25, 50, 75, 100`  
   There are **4 numbers** divisible by 25.

3. **Total frequency of 5:**  
   Adding these together:  
   `20 (from multiples of 5) + 4 (from multiples of 25) = 24`.

#### Final Answer:
The total frequency of **5** is **24**, so there are **24 trailing zeros** in **100!**.

</details>