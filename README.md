# Programming-The-Permutation_LeetCode_Solution_in_O-N-
By now, you are given a secret signature consisting of character 'D' and 'I'. 'D' represents a decreasing relationship between two numbers, 'I' represents an increasing relationship between two numbers. And our secret signature was constructed by a special integer array, which contains uniquely all the different number from 1 to n (n is the length of the secret signature plus 1). For example, the secret signature "DI" can be constructed by array [2,1,3] or [3,1,2], but won't be constructed by array [3,2,4] or [2,1,3,4], which are both illegal constructing special string that can't represent the "DI" secret signature.  On the other hand, now your job is to find the lexicographically smallest permutation of [1, 2, ... n] could refer to the given secret signature in the input.


Solution :

static int[] Permuation(String str, int N)
    {
        int min = 1;
        int max = N;
        int[] arr = new int[N];
        String[] strr = str.split("");
        int count = 0;
        for(String i : strr)
        {
            if(i.equals("D"))
            {
                arr[count] = max;
                max--;
                if(count+2 == N)
                    arr[count+1] = min;
            }
            else if(i.equals("I"))
            {
                arr[count] = min;
                min++;
                if(count+2 == N)
                    arr[count+1] = max;
            }
            count++;
        }
        return arr;
    }
