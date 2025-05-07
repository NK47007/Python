class Solution(object):
    def maxProfit(self, prices):
        if not prices:
            return 0
        
        n = len(prices)
        hold = -prices[0]
        sold = 0
        rest = 0
        
        for i in range(1, n):
            prev_hold = hold
            hold = max(hold, rest - prices[i])
            rest = max(rest, sold)
            sold = prev_hold + prices[i]
        
        return max(sold, rest)
