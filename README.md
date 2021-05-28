'''Given a non-negative number represented as a list of digits, add 1 to the number (increment the number represented by the digits). The digits are stored such that the most significant digit is first element of array.
 

Example 1:

Input: 
N = 3
arr[] = {1, 2, 4}
Output: 
1 2 5
Explanation:
124+1 = 125, and so the Output
Example 2:

Input: 
N = 3
arr[] = {9,9,9}
Output: 
1 0 0 0
Explanation:
999+1 = 1000, and so the output

Your Task:
You don't need to read input or print anything. You only need to complete the function increment() that takes an integer N, and an array arr of size N as input and returns a list of integers denoting the new number which we get after adding one to the number denoted by the array arr.


Expected Time Complexity:  O(N)
Expected Auxilliary Space: O(1)
 

Constraints:
1 <= N <= 105
0 <= arri <= 9'''




class Solution:
    def increment(self, arr, N):
        # code here
        d={1:"0",2:"00",3:"000",4:"0000",5:"00000",6:"000000",7:"0000000",9:"000000000",8:"00000000"}
        c=0
        n1=" "
        for i in arr:
            if i!=0:
                in1=arr.index(i)
                break
            c=c+1
        if c==1 and len(arr)==1:
            return str(1)
        else:
            arr1=arr[in1:]
            for i in arr1:
                n1=n1+str(i)
        if c==0:
            n1=int(n1)+1
            return str(n1)
        elif c>=1 and len(arr)>1:
            n1=int(n1)+1
            n1=d[c]+str(n1)
            return str(n1)
        
        

        

            
                
        
if __name__=='__main__':
    t=int(input())
    for _ in range(t):
        N=int(input())
        arr=list(map(int,input().split()))
        ob=Solution()
        ptr=ob.increment(arr,N)
        for i in ptr:
            print(i,end=" ")

        print()


class Solution:
    def increment(self, arr, N):
        # code here
        d={1:"0",2:"00",3:"000",4:"0000",5:"00000",6:"000000",7:"0000000",9:"000000000",8:"00000000"}
        c=0
        n1=" "
        for i in arr:
            if i!=0:
                in1=arr.index(i)
                break
            c=c+1
        if c==1 and len(arr)==1:
            return str(1)
        else:
            arr1=arr[in1:]
            for i in arr1:
                n1=n1+str(i)
        if c==0:
            n1=int(n1)+1
            return str(n1)
        elif c>=1 and len(arr)>1:
            n1=int(n1)+1
            n1=d[c]+str(n1)
            return str(n1)
        
        

        

            
                
        
if __name__=='__main__':
    t=int(input())
    for _ in range(t):
        N=int(input())
        arr=list(map(int,input().split()))
        ob=Solution()
        ptr=ob.increment(arr,N)
        for i in ptr:
            print(i,end=" ")

        print()


