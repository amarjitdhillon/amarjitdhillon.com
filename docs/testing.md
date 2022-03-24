

!!! note "A note"

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.


!!! abstract "An abstract"

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.


---



```py title="Coin Change" linenums="1"
class Solution:
    def coinChange(self, coins: List[int], amount: int) -> int:
        # Create a dp array for 0 to amount (inclusive) with the max values
        dp = [float('inf')] * (amount+1)
        
        # Initialize the value of the dp array
        dp[0] = 0
        
        # Let's compute dp array for all values from 1 to amount
        for i in range(1, amount+1):
            # We will consider all the coins and then take min from that
            for coin in coins:
                if i-coin >= 0:
                    dp[i] = min(dp[i], 1 + dp[i-coin])
        # After this loop is run, dp[amount] is our result given the fact that it's not infinity
        # If it's inf, then we will return -1
        return dp[amount] if dp[amount] != float('inf') else -1
```

The `#!python range()` function is used to generate a sequence of numbers.

$$
\operatorname{ker} f=\{g\in G:f(g)=e_{H}\}{\mbox{.}}
$$




| Method      | Description                          |
| :-----------: | :------------------------------------: |
| `GET`       |  Fetch resource  |
| `PUT`       |  Update resource |
| `DELETE`    |     Delete resource |


{%set unit_price = 100 %}

The unit price of product A is {{ unit_price }} EUR.

{{ environment.system }}