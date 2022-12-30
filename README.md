>>> data types in python==>
>>> List==>
>>>Features of list==>
>>> It is Mutable
>>>Background data structure is array.
>>> it allows Slicing, indexing 
>>>it follows sequence order
>>> l= ['Rushi',55,'Abhishek',84.4]
>>> l
['Rushi', 55, 'Abhishek', 84.4]
------------------------------------------------------
>>>Methods of list==>
>>>Append()==> Used for appending and adding elements to the end of the List
>>> l.append(10)
>>> l
['Rushi', 55, 'Abhishek', 84.4, 10]
>>> l.append([1,2])
>>> l
['Rushi', 55, 'Abhishek', 84.4, 10, [1, 2]]
>>>extend()==> used for Adds each element of the iterable to the end of the List
>>> l.extend([5,6])
>>> l
['Rushi', 55, 'Abhishek', 84.4, 10, [1, 2], 5, 6]
>>> l.extend(5)
Traceback (most recent call last):
  File "<pyshell#11>", line 1, in <module>
    l.extend(5)
TypeError: 'int' object is not iterable
>>> l.extend('string')
>>> l
['Rushi', 55, 'Abhishek', 84.4, 10, [1, 2], 5, 6, 's', 't', 'r', 'i', 'n', 'g']
>>>clear()==>This method is used for removing all items from the list. 
>>> l.clear()
>>> l
[]
>>> copy()==>
>>>shallow copy - object with same elements & having diff ids
>>> l1 = [1,2,4,5,6]
>>> l2 = l1.copy()
>>> l2
[1, 2, 4, 5, 6]
>>> id(l1)
2126962593280
>>> id(l2)
2126962595200
>>> l1.append(50)
>>> l1
[1, 2, 4, 5, 6, 50]
>>> l2
[1, 2, 4, 5, 6]
>>> # deep copy==>object with same elements & having same ids ids
>>> l3 = l1
>>> l3
[1, 2, 4, 5, 6, 50]
>>> id(l3)
2126962593280
>>> l1.append(100)
>>> l1
[1, 2, 4, 5, 6, 50, 100]
>>> l3
[1, 2, 4, 5, 6, 50, 100]
 
>>> # count()==>This methods count the elements present in the given list
>>> l1
[1, 2, 4, 5, 6, 50, 100]
>>> l1.append(2)
>>> l1
[1, 2, 4, 5, 6, 50, 100, 2]
>>> l1.count(2)
2
>>> l1.count(500)
0
>>> # insert()==>Inserts a given element at a given index in a list.
>>> #l1.insert(index number,element)
>>> l1
[1, 2, 4, 5, 6, 50, 100, 2]
>>> l1.insert(2,8)
>>> l1
[1, 2, 8, 4, 5, 6, 50, 100, 2]
>>> l1.insert(-1,20)
>>> l1
[1, 2, 8, 4, 5, 6, 50, 100, 20, 2]
>>> # insert will add element before index number
>>> len(l1)
10
>>> l1.insert(11,55)
>>> l1
[1, 2, 8, 4, 5, 6, 50, 100, 20, 2, 55]
>>> l1.insert(-11,700)
>>> l1
[700, 1, 2, 8, 4, 5, 6, 50, 100, 20, 2, 55]
>>> # pop & remove
>>> l1
[700, 1, 2, 8, 4, 5, 6, 50, 100, 20, 2, 55]
>>> # pop()==> by default it will remove last element
>>> # pop will return removed elemnt
>>> l1.pop()
55
>>> l1
[700, 1, 2, 8, 4, 5, 6, 50, 100, 20, 2]
>>> l1.pop(-3)
100
>>> l1.pop(3)
8
>>> l1
[700, 1, 2, 4, 5, 6, 50, 20, 2]
>>> l1.pop(15)
Traceback (most recent call last):
  File "<pyshell#64>", line 1, in <module>
    l1.pop(15)
IndexError: pop index out of range
>>> len(l1)
9
>>> l1.pop(2,4)
Traceback (most recent call last):
  File "<pyshell#66>", line 1, in <module>
    l1.pop(2,4)
TypeError: pop expected at most 1 argument, got 2
>>> 
>>> # remove()==>Removes a given object from the List. 
>>> # it will remove first occurance of element
>>> l1
[700, 1, 2, 4, 5, 6, 50, 20, 2]
>>> l1.remove(50)
>>> l1
[700, 1, 2, 4, 5, 6, 20, 2]
>>> l1.remove(2)
>>> l1
[700, 1, 4, 5, 6, 20, 2]

>>> # if we try to remove already removed value then it will gives value error.
>>> l1.remove(50)
Traceback (most recent call last):
  File "<pyshell#76>", line 1, in <module>
    l1.remove(50)
ValueError: list.remove(x): x not in list
>>> # int que- diff between pop & remove??
>>> l1.remove()
Traceback (most recent call last):
  File "<pyshell#78>", line 1, in <module>
    l1.remove()
TypeError: list.remove() takes exactly one argument (0 given)
>>> 
>>>  reverse==>Reverses objects of the List in place.
>>> l1
[700, 1, 4, 5, 6, 20, 2]
>>> l1[::-1]
[2, 20, 6, 5, 4, 1, 700]
>>> l1
[700, 1, 4, 5, 6, 20, 2]
>>> l1.reverse()
>>> l1
[2, 20, 6, 5, 4, 1, 700]
>>> l1
[2, 20, 6, 5, 4, 1, 700]
>>> # slicing is temporary & reverse is inplace
>>> 
>>> # sort()==>Sort a List in ascending, descending, or user-defined order
>>> # by default sort will be ascending
>>> l1
[2, 20, 6, 5, 4, 1, 700]
>>> l1.sort()
>>> l1
[1, 2, 4, 5, 6, 20, 700]

>>> s = ['a','d','f','k','g']
>>> s.sort()
>>> s
['a', 'd', 'f', 'g', 'k']
>>> h = ['a','h',22,'d',2,4,'e']
>>> h.sort()
Traceback (most recent call last):
  File "<pyshell#98>", line 1, in <module>
    h.sort()
TypeError: '<' not supported between instances of 'int' and 'str'
>>> # if we want sort in descending order
>>> l1
[1, 2, 4, 5, 6, 20, 700]
>>> l1.sort(reverse=True)
>>> l1
[700, 20, 6, 5, 4, 2, 1]
>>> l1.sort(reverse = False)
>>> l1
[1, 2, 4, 5, 6, 20, 700]
>>> l1.append(2+5j)
>>> l1
[1, 2, 4, 5, 6, 20, 700, (2+5j)]
>>> l1.sort()
Traceback (most recent call last):
  File "<pyshell#107>", line 1, in <module>
    l1.sort()
TypeError: '<' not supported between instances of 'complex' and 'int'
>>> l4 = [1+2j,4+3j,8+3j]
>>> l4
[(1+2j), (4+3j), (8+3j)]
>>> l4.sort()
Traceback (most recent call last):
  File "<pyshell#110>", line 1, in <module>
    l4.sort()
TypeError: '<' not supported between instances of 'complex' and 'complex'
>>> l1.append(5.5)
>>> l1.sort()
Traceback (most recent call last):
  File "<pyshell#112>", line 1, in <module>
    l1.sort()
TypeError: '<' not supported between instances of 'complex' and 'int'
>>> l1.remove(2+5j)
>>> l1
[1, 2, 4, 5, 6, 20, 700, 5.5]
>>> l1.append(5.5)
>>> l1.sort()
>>> l1
[1, 2, 4, 5, 5.5, 5.5, 6, 20, 700]
>>> 
>>> # reversed()
>>> # It reverse the elements of an object & output in the form of object referrence
>>> l1
[1, 2, 4, 5, 5.5, 5.5, 6, 20, 700]
>>> reversed(l1)
<list_reverseiterator object at 0x000001EF38DB2310>
>>> list(reversed(l1))
[700, 20, 6, 5.5, 5.5, 5, 4, 2, 1]
>>> l1
[1, 2, 4, 5, 5.5, 5.5, 6, 20, 700]
>>> list(reversed('rushi'))
['i', 'h', 's', 'u', 'r']
>>> s= 'rushi'
>>> s[::-1]
'ihsur'
>>> list(reversed(s))
['i', 'h', 's', 'u', 'r']
>>> ''.join(reversed(s))
'ihsur'
>>> s
'rushi'

>>> list(s)
['r', 'u', 's', 'h', 'i']
>>> sl = list(s)
>>> sl
['r', 'u', 's', 'h', 'i']
>>> sl.reverse()
>>> sl
['i', 'h', 's', 'u', 'r']
>>> ''.join(sl)
'ihsur'
>>> 
