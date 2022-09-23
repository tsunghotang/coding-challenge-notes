# Maximize Stock Trading Profit

https://www.codecademy.com/code-challenges/code-challenge-maximize-stock-trading-profit-javascript

---

Given the daily values of a stock, create a function called `maxProfitDays()` that, given a list of integers, will return the index value of the two elements that represent the day on which one should have bought a share and the day on which one should have sold a share based on the max profit.

A list of integers will represent the stock price at the beginning or “opening bell” of each day for a week. You are required to buy and sell only once. You also must buy a stock before selling it.

For example, given the list `[17, 11, 60, 25, 150, 75, 31, 120]`, you can assume that index 0 represents day 0 and index 7 represents day 7. In this case, purchasing on day 1 and selling on day 4 would yield the most profit. If we were to call `maxProfitDays([17, 11, 60, 25, 150, 75, 31, 120])`, the function would return `[1, 4]`.

---

## PEDAC

Input: array of integer

Output: array

* Return the index value of two elements that represent the days that yielded the most profit
* Index of the input array represents the days 



* Initialize `max profit` variable

* Initialize two pointers - buy and sell. 
* Calculate the profit/loss from current sell - buy. Assisgn to variable `sum`
* If `sum` is higher than the maxprofit reassign `maxProfit` Solutions

## Solutions

### JavaScript 

```javascript
function maxProfitDays(stockPrices) {
  let maxProfit = [0]

  for (let i = 0; i < stockPrices.length; i++){
    for (let j = i + 1; j < stockPrices.length; j++){
      let sum = stockPrices[j] - stockPrices[i]
      if ( sum > maxProfit[0] ) {
        maxProfit = [sum, i, j]
      }
    }
  }
	return maxProfit.slice(1)
}
```

* Initialize `maxProfit`variable set to `0`

* Iterate over the input array - `i` represents buy 
  * Inner loop - `j` represents sell - set it to always be ahead of `buy` pointer by 1
    * Initialize `sum`variable and set it to the result of sell - buy
      * IF `sum` is higher than `maxProfit`
        * Reassign `maxProfit` to an array containing the `sum` and the buy and sell pointers as elements
* Return an array containing elements at position 1 and 2