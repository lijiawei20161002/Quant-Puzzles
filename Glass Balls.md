# Glass Balls

You are holding two glass balls in a 100-story building. If a ball is thrown out of the window, it will not break if the floor number is less than `X`, and it will always break if the floor number is equal to or greater than `X`. You would like to determine `X`. What is the strategy that will minimize the number of drops for the worst-case scenario?

<details>
  <summary>Solution (click to reveal)</summary>

Suppose that we have a strategy with a maximum of `N` throws. For the first throw of ball one, we can try the `N`-th floor. If the ball breaks, we can start to try the second ball from the first floor and increase the floor number by one until the second ball breaks. At most, there are `N - 1` floors to test. So a maximum of `N` throws is enough to cover all possibilities.

If the first ball thrown from the `N`-th floor does not break, we have `N - 1` throws left. This time we can only increase the floor number by `N - 1` for the first ball, since the second ball can only cover `N - 2` floors if the first ball breaks. If the first ball thrown from the `(2N - 1)`-th floor does not break, we have `N - 2` throws left. So we can only increase the floor number by `N - 2` for the first ball, since the second ball can only cover `N - 3` floors if the first ball breaks.

Using this logic, we can see that the number of floors that these two balls can cover with a maximum of `N` throws is:

\[
N + (N - 1) + (N - 2) + \cdots + 1 = \frac{N(N + 1)}{2}
\]

To cover all 100 stories, we need:

\[
\frac{N(N + 1)}{2} \geq 100
\]

Taking the smallest integer `N` that satisfies this inequality, we find `N = 14`.

### Strategy:
1. Start by throwing the first ball from the 14th floor.
   - If the ball breaks, use the second ball to test floors 1 through 13. The maximum number of throws required is 14 (if `X` is 13 or 14).
2. If the first ball does not break, throw it from the `14 + (14 - 1) = 27`-th floor.
   - If it breaks, use the second ball to test floors 15 through 26, again requiring at most 14 throws.
3. Repeat this process, reducing the increment by one each time:
   - Next throw from `27 + (14 - 2) = 39`-th floor.
   - Then `39 + (14 - 3) = 50`-th floor, and so on.

This strategy ensures that the worst-case scenario requires a maximum of 14 throws.

</details>