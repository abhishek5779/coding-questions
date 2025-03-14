# Problem Statement

Given a linked list, determine if it exhibits a continuous mountain and valley pattern.

A continuous mountain and valley pattern is characterized by a sequence of nodes where the values consistently alternate between increasing and decreasing.

Note: if only one node, then return 1.

## Input Format

The first line contains an integer 'n' representing the number of nodes in the linked list.

The second line contains 'n' space-separated integers representing the values of the nodes in the linked list.

## Output Format

'1' indicates that the linked list follows a continuous mountain and valley pattern.

'0' indicates the linked list does not follow the continuous mountain and valley pattern.

## Constraints

- 1 <= n <= 4 * 10^3
- 0 <= elements of linked list <= 10^4

## Sample Testcase 0

**Testcase Input**
5
1 2 3 2 1

**Testcase Output**
0

**Explanation**
1 -> 2 -> 3 -> 2 -> 1
As 1 to 3 is increasing, that means values consistently do not alternate between increasing and decreasing. So the answer is 0.

## Sample Testcase 1

**Testcase Input**
5
1 2 1 2 1

**Testcase Output**
1

**Explanation**
1 -> 2 -> 1 -> 2 -> 1
As values consistently alternate between increasing and decreasing. So the answer is 1