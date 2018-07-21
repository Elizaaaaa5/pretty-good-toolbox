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
