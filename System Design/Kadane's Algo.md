Given an array of integers, find the maximum sum of subarray.
eg - [-5, 4, 6 -3, 4, -1]
Subarray which returns maximum subarray - 4, 6, -3, 4

Solutions:
1. Brute Force
```java 
public int maxSubArray(int[] nums) {

int maxSum = Integer.MIN_VALUE;

for(int i = 0; i<nums.length; i++){

int currSum = 0;

for(int j = i; j<nums.length; j++){

currSum += nums[j];

if(currSum > maxSum)

maxSum = currSum;

}

}

return maxSum;

}

//Time Complexity - O(n^2)
```


3. Kadane's Algo
To solve the problem in O(n), use below trick : keep moving ahead in the loop, but as you see the sum is negative, overall sum is negative. You discard that part there only and start moving to the next element.

Leetcode 53 - [Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
```java
int maxSum = Integer.MIN_VALUE;

int currSum = 0;

for(int i = 0; i<nums.length; i++){

currSum += nums[i];

if(currSum > maxSum)

{

maxSum = currSum;

}

if(currSum < 0)

currSum = 0;

}

return maxSum;

//Time complexity - O(n)
```

[121. Best Time to Buy and Sell Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/)

```java
class Solution {

public int maxSubArray(int[] nums) {

int maxSum = Integer.MIN_VALUE;

int currSum = 0;

for(int i = 0; i<nums.length; i++){

currSum += nums[i];

if(currSum > maxSum)

{

maxSum = currSum;

}

if(currSum < 0)

currSum = 0;

}

return maxSum;

}

}
```