## Approach

1. **Understand the Problem**:
   - You need to calculate the "wish value" for each peak, which is the absolute difference between the maximum brightness from the current peak to the highest point and the minimum brightness from the start to that peak.
   - Sum all the wish values to get the final result.

2. **Initialize Data Structures**:
   - Use one array and one variable to store the maximum brightness from the current peak to the highest point (`max_right`) and variable for the minimum brightness from the start to that peak (`min_left`).

3. **Calculate `max_right` Array**:
   - Traverse the array from right to left to fill the `max_right` array with the maximum brightness values.

4. **Calculate `min_left` Value & Wish Value**:
   - Traverse the array from left to right and identify the `min_left` value for the current peak with the minimum brightness values.
   - Iterate through each peak and calculate the wish value using the `max_right` array and `min_left` variable.
   - Sum all the wish values.

5. **Return the Result**:
   - Print the sum of all wish values.