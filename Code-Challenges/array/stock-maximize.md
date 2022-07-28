Your algorithms have become so good at predicting the market that you now know what the share price of Wooden Orange Toothpicks Inc. (WOT) will be for the next number of days.

Each day, you can either buy one share of WOT, sell any number of shares of WOT that you own, or not make any transaction at all. What is the maximum profit you can obtain with an optimum trading strategy?

Example:
```
prices = [5, 3, 2]
There is no profit because the share price never rises, return 0.

prices = [1, 2, 100]
Buy one share on the first two days and sell both of them on the third day for a profit of 197.

prices = [1, 3, 1, 2]
Buy one share on day 1, sell one on day 2, buy one share on day 3, and sell one share on day 4. The overall profit is 3.
```

Solutions:
```python
def find_solution(prices):
    max_price = max(prices)
    profit = 0
    days_long = 0
    while len(prices) > 0:
        day_price = prices.pop(0)
        if day_price == max_price:
            profit += day_price * days_long
            days_long = 0
            if len(prices):
                max_price = max(prices)
        elif day_price < max_price:
            profit -= day_price
            days_long += 1
    return profit


assert find_solution([5, 3, 2]) == 0
assert find_solution([1, 2, 100]) == 197
assert find_solution([1, 3, 1, 2]) == 3
```
