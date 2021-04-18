TARGET DECK: Scipy_lecture

the key concept here is mutable vs. immutable #flashcard 
– mutable objects can be changed in place
– immutable objects cannot be modified once created
<!--ID: 1618091783212-->

Sets Vs Tuples #flashcard 
Tuples
Tuples are basically immutable lists. The elements of a tuple are written between parentheses, or just
separated by commas:
>>> t = 12345, 54321, 'hello!'
>>> t[0]
12345
>>> t
(12345, 54321, 'hello!')
>>> u = (0, 2)
**Sets: unordered, unique items:**
>>> s = set(('a', 'b', 'c', 'a'))
>>> s
set(['a', 'c', 'b'])
>>> s.difference(('a', 'b'))
set(['c'])
<!--ID: 1618091941728-->

For i in range(4): #flashcard 
Iterating with an index:
>>> for i in range(4):
... print(i)
0123
<!--ID: 1618092013532-->

for word in ('cool', 'powerful', 'readable'): #flashcard 
... print('Python is %s ' % word)
Python is cool
Python is powerful
Python is readable
<!--ID: 1618092046300-->

While/Break/Continue #flashcard 
![[Pasted image 20210410180731.png]]
<!--ID: 1618092454216-->


Conditional expression #flashcard 
![[Pasted image 20210410180825.png]]
<!--ID: 1618092508567-->


Advance iteration #flashcard 
![[Pasted image 20210410181137.png]]
<!--ID: 1618092701161-->

Enumeration Number #flashcard 
![[Pasted image 20210410181330.png]]
<!--ID: 1618092819133-->

Sorting through dictionaries #flashcard 
![[Pasted image 20210410181428.png]]
<!--ID: 1618092872056-->


List comprehensions #flashcard 
![[Pasted image 20210410181520.png]]
<!--ID: 1618092923653-->

optional parameters in a function #flashcard 
![[Pasted image 20210410181741.png]]
<!--ID: 1618093062612-->

Python Slicing #flashcard 
![[Pasted image 20210410181848.png]]
<!--ID: 1618093132359-->


What are Global variables #flashcard 
![[Pasted image 20210410182007.png]]
<!--ID: 1618093211810-->

\*args  \*kwargs #flashcard 
![[Pasted image 20210410182216.png]]
<!--ID: 1618093340030-->

Docstrings when using functions #flashcard 
![[Pasted image 20210410182254.png]]
<!--ID: 1618093376896-->

Functions are Objects, but why #flashcard 
Functions are first-class objects, which means they can be:
- assigned to a variable
-  an item in a list (or any collection)
- passed as an argument to another function.
>>> In [38]: va = variable_args
>>> In [39]: va('three', x=1, y=2) 
____
args is ('three',)
kwargs is {'x': 1, 'y': 2}
<!--ID: 1618093887310-->

what are methods #flashcard 
Methods are functions attached to objects. You’ve seen these in our examples on lists, dictionaries,
strings, etc. . .
<!--ID: 1618093960153-->

Style guidelines #flashcard 
![[Pasted image 20210410183736.png]]
<!--ID: 1618094259540-->

Creating arrays #flashcard 
![[Pasted image 20210410184611.png]]
<!--ID: 1618094773940-->

slicing #flashcard 
![[Pasted image 20210410184933.png]]
<!--ID: 1618094976406-->

slicing V2 #flashcard 
![[Pasted image 20210410185016.png]]
<!--ID: 1618095019054-->

copies and views #flashcard 
![[Pasted image 20210410185756.png]]
<!--ID: 1618095479422-->
  
Fancy Indexing #flashcard 
#### Tip: NumPy arrays can be indexed with slices, but also with boolean or integer arrays (masks). 
method is called fancy indexing. **It creates copies not views.**
![[Pasted image 20210410205338.png]]
![[Pasted image 20210410205611.png]]
<!--ID: 1618102613716-->

Axis = 0, axis=1, axis =2  #flashcard 
![[Pasted image 20210410210226.png]]
<!--ID: 1618102947482-->

Logical Operations #flashcard 
![[Pasted image 20210410210350.png]]
<!--ID: 1618103039428-->

Np statistics #flashcard 
![[Pasted image 20210410210443.png]]
<!--ID: 1618103085697-->

Argmax, argmin  #flashcard 
>>> a = np.array([4, 3, 1, 2])
>>> j_max = np.argmax(a)
>>> j_min = np.argmin(a)
>>> j_max, j_min
(0, 2)
<!--ID: 1618103655829-->


how to enter matplotlib mode #flashcard 
%matplotlib inlin
<!--ID: 1618153814108-->

Import matplotlib #flashcard 
from matplotlib import pyplot as plt 
<!--ID: 1618153862178-->


Removing ticks #flashcard 
ax = plt.gca() # gca stands for 'get current axis'
ax.spines['right'].set_color('none')
ax.spines['top'].set_color('none')
ax.xaxis.set_ticks_position('bottom')
ax.spines['bottom'].set_position(('data',0))
ax.yaxis.set_ticks_position('left')
ax.spines['left'].set_position(('data',0))
<!--ID: 1618161033885-->


how to add a legend to the graph #flashcard 
plt.legend(loc="location")
<!--ID: 1618161082480-->

what are all the figures in matplotlib #flashcard 
![[Pasted image 20210411131326.png]]
<!--ID: 1618161217605-->

Percentiles with stats #flashcard 
![[Pasted image 20210411154741.png]]
<!--ID: 1618170463273-->

Removing spines from graphs #flashcard 
![[Pasted image 20210411161214.png]]
![[Pasted image 20210411161320.png]]
<!--ID: 1618171938265-->

what does alpha do in matplotlib #flashcard 
![[Pasted image 20210411161253.png]]
<!--ID: 1618172005546-->

How to remove ticks and all spines #flashcard 
![[Pasted image 20210411161410.png]]
<!--ID: 1618172063398-->

adding a rectangle and annotate #flashcard 
![[Pasted image 20210411161556.png]]
<!--ID: 1618172158716-->

Axhspan and axvspan #flashcard 
![[Pasted image 20210411161745.png]]
<!--ID: 1618172268779-->

using fill_between #flashcard 
![[Pasted image 20210411161818.png]]
<!--ID: 1618172303613-->

Annotating with Boxplots #flashcard 
![[Pasted image 20210417170809.png]]
<!--ID: 1618693746846-->


Using text in BarPlot #flashcard 
![[Pasted image 20210417170903.png]]
![[Pasted image 20210417170948.png]]
<!--ID: 1618693746890-->

RelPlot Vs disPlot Vs Catplot SNS #flashcard 
![[Pasted image 20210417171102.png]]
<!--ID: 1618693911905-->


How to Use GridSpec #flashcard 
![[Pasted image 20210417171221.png]]
![[Pasted image 20210417171241.png]]
<!--ID: 1618693962679-->







