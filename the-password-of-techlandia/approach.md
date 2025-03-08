## Approach

1. **Understand the Problem**:
   - You need to check if every number in the password appears an even number of times.
   - At least one number must appear exactly twice.
   - Identify the most frequent element in the password.

2. **Initialize Data Structures**:
   - Use a hash map (or dictionary) to count the frequency of each element in the password array.

3. **Count Frequencies**:
   - Iterate through the password array and update the frequency count for each element in the hash map.

4. **Check Conditions**:
   - Iterate through the hash map to check if every number appears an even number of times.
   - Check if at least one number appears exactly twice.

5. **Identify the Most Frequent Element**:
   - Track the element with the highest frequency.
   - If multiple elements have the same highest frequency, select the smallest one.

6. **Output the Result**:
   - Print "VALID" if the conditions are met; otherwise, print "INVALID".
   - Print the most frequent element.