### Bubble sort

```python
# Python code to sort the lists using the second element of sublists 
# Inplace way to sort, use of third variable 
def Sort(sub_li): 
    l = len(sub_li) 
    for i in range(0, l): 
        for j in range(0, l-i-1): 
            if (sub_li[j][1] > sub_li[j + 1][1]): 
                tempo = sub_li[j] 
                sub_li[j]= sub_li[j + 1] 
                sub_li[j + 1]= tempo 
    return sub_li 
  
# Driver Code 
sub_li =[['rishav', 10], ['akash', 5], ['ram', 20], ['gaurav', 15]] 
print(Sort(sub_li)) 

Output:

[['akash', 5], ['rishav', 10], ['gaurav', 15], ['ram', 20]]

```

###Method 2: Sorting by the use of sort() method

While sorting via this method the actual content of the tuple is changed, and just like the previous method, in-place method of sort is performed.

filter_none
edit
play_arrow

brightness_4

```python
# Python code to sort the tuples using second element  
# of sublist Inplace way to sort using sort() 
def Sort(sub_li): 
  
    # reverse = None (Sorts in Ascending order) 
    # key is set to sort using second element of  
    # sublist lambda has been used 
    sub_li.sort(key = lambda x: x[1]) 
    return sub_li 
  
# Driver Code 
sub_li =[['rishav', 10], ['akash', 5], ['ram', 20], ['gaurav', 15]] 
print(Sort(sub_li)) 
Output:

[['akash', 5], ['rishav', 10], ['gaurav', 15], ['ram', 20]]

```

###Method 3: Sorting by the use of sorted() method

Sorted() sorts a list and always returns a list with the elements in a sorted manner, without modifying the original sequence. It takes three parameters from which two are optional, here we tried to use all of the three:

Iterable : sequence (list, tuple, string) or collection (dictionary, set, frozenset) or any other iterator that needs to be sorted.
Key(optional) : A function that would server as a key or a basis of sort comparison.
Reverse(optional) : To sort this in ascending order we could have just ignored the third parameter, which we did in this program. If set true, then the iterable would be sorted in reverse (descending) order, by default it is set as false.
filter_none
edit
play_arrow

```python
# Python code to sort the tuples using second element  
# of sublist Function to sort using sorted() 
def Sort(sub_li): 
  
    # reverse = None (Sorts in Ascending order) 
    # key is set to sort using second element of  
    # sublist lambda has been used 
    return(sorted(sub_li, key = lambda x: x[1]))     
  
# Driver Code 
sub_li =[['rishav', 10], ['akash', 5], ['ram', 20], ['gaurav', 15]] 
print(Sort(sub_li)) 
Output:

[['akash', 5], ['rishav', 10], ['gaurav', 15], ['ram', 20]]

```
