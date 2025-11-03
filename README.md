class Solution(object):
    def climbStairs(self, n):
        """
        :type n: int
        :rtype: int
        """
        if n <= 2:
            return n  # If n is 1 or 2, return n directly (base cases)
        
        first, second = 1, 2  # Initialize base cases: ways to reach step 1 and 2
        
        for i in range(3, n + 1):
            current = first + second  # The current step depends on the last two steps
            first, second = second, current  # Update the two previous steps for the next iteration
        
        return second
        
