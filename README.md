# PROJECT-5
 import java.util.* ;

import java.io.*; 

public class Solution {
    
    public static long maxSubarraySum(int[] arr, int n) {
        // write your code here
        // Initialize maxEnding with the first element of the array
         long maxEnding = arr[0];
        // Initialize maxSoFar with the first element of the array
         long maxSoFar = arr[0]; 

        for (int i = 1; i < n; i++) {
            maxEnding = Math.max(arr[i], maxEnding + arr[i]);
            maxSoFar = Math.max(maxSoFar, maxEnding);
        }

        if (maxSoFar < 0) {
            // If all elements are negative, return 0 (empty subarray)
            return 0; 
        }

        return maxSoFar;
    }

}
Input: 'arr' = [1, 2, 7, -4, 3, 2, -10, 9, 1]

Output: 11

Explanation: The subarray yielding the maximum sum is [1, 2, 7, -4, 3, 2].
Sample Input 2 :
6
10 20 -30 40 -50 60


Sample Output 2 :
60
