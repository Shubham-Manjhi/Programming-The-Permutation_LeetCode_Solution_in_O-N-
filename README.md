# Programming - 484 The Permutation LeetCode Solution in O(N)
By now, you are given a secret signature consisting of character 'D' and 'I'. 'D' represents a decreasing relationship between two
numbers, 'I' represents an increasing relationship between two numbers. And our secret signature was constructed by a special integer
array, which contains uniquely all the different number from 1 to n (n is the length of the secret signature plus 1). For example, the
secret signature "DI" can be constructed by array [2,1,3] or [3,1,2], but won't be constructed by array [3,2,4] or [2,1,3,4], which are
both illegal constructing special string that can't represent the "DI" secret signature.  On the other hand, now your job is to find the
lexicographically smallest permutation of [1, 2, ... n] could refer to the given secret signature in the input.


Solution :

![image](https://user-images.githubusercontent.com/66024002/148218197-1d4cf73f-e365-4599-ba16-f11346e1cf31.png)
