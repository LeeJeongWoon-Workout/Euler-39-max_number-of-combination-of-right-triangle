# Euler-39-max_number-of-combination-of-right-triangle

import math

def number(n):
    t=0
    for i in range(n//2):
       for j in range(n//2):
           result=i*i+j*j
           result=math.sqrt(result)
           if int(result)==result and result+i+j==n:
               t+=1
    return t/2

max=0
for i in range(1,1001):
    n=number(i)
    if max<n:
        max=n
        print(max,i)
