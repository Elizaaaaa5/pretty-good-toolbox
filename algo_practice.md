1. hamming distance
```
#Luyao's solution
class Solution(object):
    def hammingDistance(x, y):
        """
        :type x: int
        :type y: int
        :rtype: int
        """
        # bin_x=int(bin(x)[2:])
        # bin_y=int(bin(y)[2:])
        # print(bin_x)
        # print(bin_y)
        # print(str(bin_x^bin_y))
        print(x^y)
        return(str(bin(x^y)).count('1'))

        # print((str(bin_x^bin_y)).count('1'))

    hammingDistance(93,73)

#4ms faster optimized solution
class Solution(object):
    def hammingDistance(self, x, y):
        """
        :type x: int
        :type y: int
        :rtype: int
        """
        a=x^y
        t=int(0)
        while a>0:
            if  a%2==1:
                a=a-1
                t=t+1
            elif a%2==0:
                a=a//2
        return t
```

2. Hamming Weight
```
#Write a function that takes an unsigned integer and returns the number of '1' bits it has (also known as the Hamming weight).
class Solution(object):
    #Luyao's solution
    def hammingWeight(n):
        """
        :type n: int
        :rtype: int
        """
        #since we are just counting 1, just slice out '0b'
        return str(bin(n))[2:].count('1')
    hammingWeight(2) 
```

3. Majority number in an array  
    geekforgeek[https://www.geeksforgeeks.org/majority-element/]  
    > If we cancel out each occurrence of an element e with all the other elements that are different from e then e will exist till end if it is a majority element. Loop through each element and maintains a count of the element that has the potential of being the majority element. If next element is same then increments the count, otherwise decrements the count. If the count reaches 0 then update the potential index to the current element and reset count to 1.  
    ```
    # C++
        class Solution {
        public:
            int majorityElement(vector<int> &num) {
                int majorityIndex = 0;
                for (int count = 1, i = 1; i < num.size(); i++) {
                    num[majorityIndex] == num[i] ? count++ : count--;
                    if (count == 0) {
                        majorityIndex = i;
                        count = 1;
                    }
                }

                return num[majorityIndex];
            }
    };
    
    # Java
        public class Solution {
        public int majorityElement(final List<Integer> A) {
            
            if (A == null)
                return -1;
                
            int maj = A.get(0);
            int count = 1;
            int n = A.size();
            
            for (int i = 1; i < n; i++) {
                if (A.get(i) == maj) {
                    count++;
                } else if (count == 1) {
                    maj = A.get(i);
                } else {
                    count--;
                }
            }
            
            count = 0;
            
            for (int i = 0; i < n; i++) {
                if (A.get(i) == maj)
                    count++;
            }
            
            if (count > n / 2)
                return maj;
                
            return -1;
            
            
        }
    }

    # Python
    class Solution:
        # Function to check if the candidate occurs more than n/2 times
        def majorityElement(Self, A):
            major = 0
            for i in xrange(len(A)):
                major = A[i]
                count = 1
                for j in xrange(i + 1, len(A)):
                    if A[j] == major:
                        count += 1
                if count > len(A)/2:
                    return major
            return -1
    ```



