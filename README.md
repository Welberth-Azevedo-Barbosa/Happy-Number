# Happy-Number
Solution for "Happy number"

# Happy Number Checker

This Python code checks whether a number is a "happy number" based on the following requirements:

- Starting with any positive integer, replace the number by the sum of the squares of its digits.

- Repeat the process until the number equals 1 (where it will stay), or it loops endlessly in a cycle that does not include 1.

- Numbers for which this process ends in 1 are considered happy.

# Implementation

The code is implemented in the Solution class, which provides a method called isHappy. This method takes a positive integer n as an argument and returns a boolean value indicating whether n is a happy number or not.

# Algorithm

The algorithm used in the code is as follows:

Create an empty set called mem to store the numbers encountered during the process.

Enter a while loop that continues until the number n becomes 1.

Inside the loop, calculate the next value of n by summing the squares of its digits. This is done by converting n to a string, iterating over each digit, converting it back to an integer, and squaring it. The resulting sum becomes the new value of n.

Check if the new value of n already exists in the mem set. If it does, it means we have entered an endless cycle and n is not a happy number. In this case, return False to indicate that the number is not happy.

If the new value of n is not in the mem set, add it to the set to keep track of the encountered numbers.

If the while loop terminates because n is equal to 1, it means we have found a happy number. Return True to indicate that the number is happy.

# Usage

To use the isHappy function, create an instance of the Solution class and call the method, passing a positive integer as an argument. The function will return True if the number is happy and False otherwise.

# Example usage:

# python
solution = Solution()  
result = solution.isHappy(19)   
print(result)  # Output: True

In the above example, the code checks whether the number 19 is a happy number. The output will be True because the process eventually leads to 1.

# Complexity Analysis
The time complexity of the code is dependent on the number of digits in the input number n. Let d be the number of digits in n. In the worst case, the process might require iterating through all the digits of n and calculating the sum of their squares. Therefore, the time complexity is O(d).

The space complexity is also dependent on the number of digits in n. In the worst case, if the process enters an endless cycle, the mem set can potentially store all the numbers encountered, which can be up to O(d) elements. Hence, the space complexity is O(d).
