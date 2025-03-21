# Two Sum LeetCode Problem

## Summarize

The Two Sum problem is a classic problem on LeetCode where you are given an array of integers and a target sum, and you need to find two elements in the array that add up to the target sum. The problem requires you to return the indices of the two elements.

## Approach

To solve this problem, we can use a hash table to store the elements of the array as we iterate through it. For each element, we check if its complement (i.e., the value that would add up to the target sum) is already in the hash table. If it is, we return the indices of the current element and its complement. If not, we add the current element to the hash table and continue iterating.

Here is the JavaScript code for the solution:

```javascript
function twoSum(nums, target) {
  const numToIndex = new Map();
  for (let i = 0; i < nums.length; i++) {
    const complement = target - nums[i];
    if (numToIndex.has(complement)) {
      return [numToIndex.get(complement), i];
    }
    numToIndex.set(nums[i], i);
  }
  return null;
}
```  
