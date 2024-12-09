# Coin Piles

Suppose that you are blindfolded in a room and are told that there are 1000 coins on the floor. 980 of the coins have tails up, and the other 20 coins have heads up. Can you separate the coins into two piles so that both piles have an equal number of heads? Assume that you cannot tell a coin's side by touching it, but you are allowed to turn over any number of coins.

<details>
  <summary>Solution (click to reveal)</summary>

Let's say that we separate the 1000 coins into two piles with `n` coins in one pile and `1000 - n` coins in the other. If there are `m` coins in the first pile with heads up, there must be `20 - m` coins in the second pile with heads up. We also know that there are `n - m` coins in the first pile with tails up. 

Clearly, we cannot guarantee that `m = 10` by simply adjusting `n`.

### Exploring Other Options

We can turn over coins if we want to. Since we have no way of knowing what a coin's side is, selectively flipping coins won’t guarantee anything. However, if we flip **all** the coins in the first pile, all heads become tails and all tails become heads. As a result, the first pile will have `n - m` heads and `m` tails due to symmetry.

To achieve equal heads in both piles, we need the number of tails in the original first pile to equal the number of heads in the second pile. This requires:

\[
n - m = 20 - m
\]

Solving for `n`:

\[
n = 20
\]

Thus, the solution is to:
1. Take **20 coins at random** and put them in the first pile.
2. Turn over **all** 20 coins in the first pile.
3. The remaining 980 coins form the second pile.

The number of heads among the flipped 20 coins will always equal the number of heads among the other 980 coins, ensuring that both piles have an equal number of heads.

</details>