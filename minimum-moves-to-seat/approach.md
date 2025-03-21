# Minimum Moves to Seat

## 1. Understand the Problem Statement
You are given two arrays:
- `seats`: Positions of the seats.
- `students`: Positions of the students.

The goal is to move students to seats such that:
- Each student is assigned to one seat.
- The total number of moves is minimized.
- A move is defined as shifting a student one position to the left or right.

---

## 2. Key Observations
- To minimize the number of moves, each student should be assigned to the closest available seat.
- Sorting both arrays ensures that the smallest seat is paired with the smallest student, the second smallest seat with the second smallest student, and so on. This minimizes the distance between each student and their assigned seat.

---

## 3. Plan the Solution

### Input:
- Read the number of seats/students (`N`).
- Read the `seats` and `students` arrays.

### Sort the Arrays:
- Sort both `seats` and `students` in ascending order.

### Calculate Moves:
- Iterate through the sorted arrays.
- For each pair of `seats[i]` and `students[i]`, calculate the absolute difference (`|seats[i] - students[i]|`) and add it to a running total.

### Output:
- Print the total number of moves.

---

## 4. Algorithm
1. Sort the `seats` array.
2. Sort the `students` array.
3. Initialize `total_moves` to 0.
4. Loop through the arrays and calculate the sum of absolute differences.
5. Return or print the result.

---

## 5. Example Walkthrough

### Input:
N = 5
seats = [1, 3, 5, 7, 9]
students = [2, 4, 6, 8, 10]

### Steps:
Sort seats: [1, 3, 5, 7, 9]
Sort students: [2, 4, 6, 8, 10]
Calculate total moves:
|1 - 2| = 1
|3 - 4| = 1
|5 - 6| = 1
|7 - 8| = 1
|9 - 10| = 1
Total moves = 1 + 1 + 1 + 1 + 1 = 5
Output:
5

---

## 6. Complexity Analysis
### Time Complexity:
- Sorting both arrays: (O(N \log N)).
- Calculating total moves: (O(N)).
- Total: (O(N \log N)).

### Space Complexity:
- Sorting is done in-place, so space complexity is (O(1)) (excluding input storage).