# Mislabeled Bags

You are given three bags of fruits. One has apples in it, one has oranges in it, and one has a mix of apples and oranges in it. Each bag has a label on it (apple, orange, or mix). Unfortunately, your manager tells you that **ALL bags are mislabeled**. Develop a strategy to identify the bags by taking out the minimum number of fruits. You can take any number of fruits from any bags.

<details>
  <summary>Solution (click to reveal)</summary>

The key insight here is to use the fact that **ALL bags are mislabeled**. For example, a bag labeled with "apple" must contain either oranges only or a mix of oranges and apples.

Let's analyze the situation:
- Labels: **orange**, **apple**, and **mix** (orange + apple).
- Mislabeling ensures that the bag labeled "orange" does not contain oranges only, the bag labeled "apple" does not contain apples only, and the bag labeled "mix" does not contain a mix.

### Strategy

1. Start with the bag labeled as **mix**.
   - Since this bag cannot actually contain a mix (due to mislabeling), it must contain either **only apples** or **only oranges**.
   - Pick one fruit from this bag.

2. Based on the fruit picked:
   - If the fruit is an **orange**, then the bag labeled "mix" is actually the **orange-only** bag.
   - If the fruit is an **apple**, then the bag labeled "mix" is actually the **apple-only** bag.

3. Use the information from the mislabeled bag to deduce the contents of the other bags:
   - If the bag labeled "mix" contains oranges:
     - The bag labeled "apple" cannot be the apple-only bag, so it must be the **mix** bag.
     - The bag labeled "orange" must be the **apple-only** bag.
   - Similarly, if the bag labeled "mix" contains apples:
     - The bag labeled "orange" cannot be the orange-only bag, so it must be the **mix** bag.
     - The bag labeled "apple" must be the **orange-only** bag.

### Conclusion

By taking just **one fruit** from the bag labeled as "mix," you can determine the true contents of all three bags. This strategy minimizes the number of fruits needed to solve the problem.