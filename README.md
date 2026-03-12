class Solution:
    def frequencyCount(self, arr):
        n = len(arr)
        # Initialize the result array of size n with 0s
        # res[i] will store the frequency of (i + 1)
        res = [0] * n
        
        # Count the frequency of each element
        for x in arr:
            # Check if x is within the range [1, n]
            # (Though constraints say it will be, it's good practice)
            if 1 <= x <= n:
                res[x - 1] += 1
                
        return res

# Example Trace:
# arr = [2, 3, 2, 3, 5], n = 5
# res = [0, 0, 0, 0, 0]
# Process 2 -> res[1] becomes 1
# Process 3 -> res[2] becomes 1
# Process 2 -> res[1] becomes 2
# Process 3 -> res[2] becomes 2
# Process 5 -> res[4] becomes 1
# Result: [0, 2, 2, 0, 1]
