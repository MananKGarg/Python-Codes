## Functions
---

1. help() function - find what a function does
                   - print takes sep as an argument, for example print("hello", "world", sep='>')
                   
2. defining our own functions - def

                   ```python
                   
                   def least_difference(a,b,c):
                       diff1 = abs(a-b)
                       diff2 = abs(b-c)
                       diff3 = abs(c-a)
                       return min(diff1,diff2,diff3)
                       ```
