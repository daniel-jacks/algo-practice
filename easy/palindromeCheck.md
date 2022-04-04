# Problem Domain
Write a function that takes in a non-empty string and that returns a boolean representing whether the string is a palindrome. 

## Hypothesis
- I want to iterate through the string using a for loop, and while doing that using a frequency counter to track values of letters within the string.
- The frequency counter will be ADDED to while going through the first half of the string, and then SUBTRACTED from when going through the second half. 
- Different checks will be used along the way, depending on if we are going 'forward' (first half of string) or 'backward' (second half of string). \
- When subtracting we will check if a value is truthy within the freq counter, and if it is truthy we will subtract from it, and if it's falsey, we will return false. 

## BigO
- Time is equal to O(n), because we are iterating through the entire string at worst.
- Space is equal to O(log(n)), because we will only ever store HALF the values within the string in our frequency counter. 

## Key Takeaways
- Keep working with your solution if you think it's the right direction. Worst case, you have a better understanding if you're right, and a great learning opportunity if you're wrong.