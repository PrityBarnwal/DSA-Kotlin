# Best Time to Buy and Sell Stock II
## Overview

```ruby
fun maxProfit(prices:IntArray):Int{
    if(prices.isEmpty()) return 0

    var minPrice = prices[0]
    var maxProfit = 0

    for(i in 1 until prices.size){
        var price = prices[i]
         // Calculate profit if selling at the current price
        val profit =price - minPrice

         // Update maxProfit if this profit is greater
         if(profit > maxProfit){
            maxProfit = profit
         }

         // Update minPrice if a lower price is found
         if(profit < minPrice){
            minPrice = price
         }
    }
    return maxProfit
}
```
```ruby
fun main() {
    val prices = intArrayOf(7, 1, 5, 3, 6, 4)
    println("Max Profit: ${maxProfit(prices)}")
}
```

# OutPut
```ruby
Max Profit: 5
```