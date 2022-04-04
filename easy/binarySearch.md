# Problem Domain
Write a function that takes in a sorted array of integers as well as a target integer. The function should use the Binary Search algorithm to determine if the target integer is contained in the array and should return its index if it is, otherwise, return -1. 

## Hypothesis
- I believe the best way to work this problem through will be using recursion. That does mean that the space complexity will most likely be greater than if we did iterative approach, but I think using recursion will make the code look cleaner. 
- First, we have to start with a 'left' and a 'right', which will be pointing at the start and end of the array, respectively. 
- Second, finding the 'middle' of the array or sub array will be important, and in order to do this dynamically, you can add up the index of start and end, and average them out. 
- From here you simply need to compare the middle value, and dynamically change the sub array you are targeting, as well as the 'middle' variables. - Continue this until you either find your target, or 'left' is greater than 'right', meaning you have covered every element within the array.

## BigO
- Time is equal to O(log(n)), with n being the length of the array. This is because after every iteration, you are splitting the array in half. If you are ever splitting the input in half (like binary array or search tree) think log(n).
- Space is dependant upon if you choose recursive or iterative approach (iterative is better in most cases). If recursive, O(log(n)), because each time you call the recursive function, it's taking up another space in the call stack. Iterative is O(1) because you don't create any new space.

## Key Takeaways
- You must be working with a sorted array for this to work
- When checking if a middle value is equal to your target value, keep in mind that if it is not, and you are changing your sub array, you have already covered the current middle value, meaning you should be either to the right or left of that value for your next sub array.