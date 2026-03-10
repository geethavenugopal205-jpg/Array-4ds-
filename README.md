class Solution:
    def getSecondLargest(self, arr):
        # Initialize largest and second largest to -1
        largest = -1
        second_largest = -1
        
        for x in arr:
            # If current element is greater than the largest
            if x > largest:
                second_largest = largest
                largest = x
            # If current element is between largest and second largest
            elif x > second_largest and x != largest:
                second_largest = x
                
        return second_largest
        
