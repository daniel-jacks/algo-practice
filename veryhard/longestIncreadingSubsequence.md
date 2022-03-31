# Problem Domain
Given a non-empty array of integers, write a function that returns the longest strictly-increasing subsequence in the array. m

## Hypothesis
- There are a few things you need to track here, and I believe using a parallel array might help with tracking values as you traverse of the input array. 
- The BigO of time is difficult to make efficient, because with this solution you would have to be looking at all previous values as you get to each new element within the input array.

## Solution
- Use two arrays as you traverse through the the input array. The lengths array is tracking the length of the longest subsequence you can build from that index of the array, and the sequences array is tracking the index of the previous value from that longest subsequence. 
- Once you have iterated through all of the elements of the array, you will have two arrays filled with data. From their, you can start working backwards from the lengths array, starting at the highest value. 
- While building your outputArray, you will want to use a parellel array technique to get the value from the input array at that index, and unshift it into your outputArray, THEN use your sequences array to get the next index you are trying to target.

## BigO
- Time is equal to O(n^2), because at worst you will be working through all of the previous elements of the array at each index. 
- Space is going to be O(2n), simplified to O(n) because we are creating two arrays with equal lenth to our input array.

## Key Takeaways
- Brute forcing this algorithm is the cleanest way to do it, although it is not the most time efficient. 
- Don't be afraid to brute force it, come up with a good solution and be able to code it out and then make the solution better if possible in the time allotted. 
- Using parallel arrays for solving array problems can be very powerful. 