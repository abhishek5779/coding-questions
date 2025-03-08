## Approach

1. **Understand the Problem**:
   - You need to find pairs of stones such that each number in the pair is divisible by either N or M.
   - Ensure no pair is repeated and each pair contains different stones.

2. **Brute force approach**:
   - Use a nested loop to generate all possible pairs and count the valid ones.
   - Ensure that each pair contains different stones and is not repeated.
   - Count the number of valid pairs that meet the criteria.

3. **Optimized approach**:
   - Iterate through the list of stones and add those that are divisible by N or M to the set/vector.
   - Instead of storing those eligible stones to the set/vector, we can only keep count of them.
   - Then to identify the final result, we can use the formula `validcount*(validcount-1)/2`

4. **Output the Result**:
   - Print the count of valid pairs.