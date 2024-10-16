Common elements in all rows of a given matrix in Python
Here, on this page, we will discuss the program to find the Common elements in all rows of a given matrix in Python Programming language.

Common elements in all rows of the matrix

Algorithm ( Method 1 )
In this algorithm, we will check for every element in the first row, if that is present in other rows or not.

For checking the presence, take one variable count.
Now, run a loop from index 1 to M.
Take a variable flag =0;
Now, run a loop from index 0 to N, if (x==mat[i][j]) set flag =1 and break the loop.
After coming out from loop check if(flag==1) set, count++.
At last, check if count == M-1, print that value.
Time and Space Complexity :
Time complexity: O(M*M*N)
Space complexity: O(1)
Common elements in all rows of the matrix in Python
Python Code
Run
def find(mat, N, M):
    for j in range(0, N):
        x, count = mat[0][j], 0

        for i in range(1, M):
            flag = 0
            for k in range(0, N):
                if x == mat[i][k]:
                    flag = 1
                    mat[i][k] = -1
                    break
            if flag == 1:
                count += 1
        if count == M - 1:
            print(x)


N, M = 4, 4
mat = [[10, 20, 30, 40],
       [15, 25, 35, 30],
       [27, 30, 37, 48],
       [32, 33, 39, 30]]
find(mat, N, M)
Output
30
