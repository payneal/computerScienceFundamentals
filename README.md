# Google Prep Course (python version)

## 1.) watch these 2 videos
* https://www.youtube.com/watch?v=qc1owf2-220&feature=youtu.be
* https://www.youtube.com/watch?v=oWbUtlUhwa8&feature=youtu.be

## 2.) Review your past jobs and side projects
* Think of all the things you did that were instering, then think of the most  most interesting solutions you came up to sovle the issue at hand
* google says this: 
Your background is important, so utilize it to your advantage by sharing interesting points that can help you and the engineer work through the discussion as efficient as possi

__## Computer Science fundementals__

## 3.) Algorithum Complexity 
* big-o notaion (must know or you will fail)
big-o-notation =  A theoretical measure of the execution of an algorithm, usually the time or memory needed, given the problem size n, which is usually the number of items. Informally, saying some equation f(n) = O(g(n)) means it is less than some constant multiple of g(n).

![Table](/../master/images/bigo.png?raw=true "Algorithum table")
![Graph](/../master/images/bigograph.png??raw=true "Graph")

* https://www.topcoder.com/blog/big-o-notation-primer/  

O(1) = O(1) represents an algorithm that takes the same amount of time to execute regardless of the number of inputs. So, 1 item takes 1 second, 10 items take 1 second, 100 items take 1 second and so on. Therefore performance is not affected by the size of the input data.

O(N) = O(N) represents an algorithm where the size of the input data impacts the execution time. The performance of the algorithm is directly proportional to the number of inputs. So, 1 item takes 1 second, 10 items take 10 seconds, 100 items take 100 seconds and so on.

O(log N) = O(log N) represents an algorithm where the number of computations grows linearly as input data grows exponentially. So 1 item takes 1 second, 10 items take 2 seconds, 100 items take 3 seconds and so on.

O(2N) = O(2N) represents an algorithm where execution time is doubled for each additional input. So 1 item takes 2 seconds, 2 items take 4 seconds, 3 items take 8 seconds and so on.

O(N!) = O(N!) represents a factorial algorithm that must perform N! calculations. So 1 item takes 1 second, 2 items take 2 seconds, 3 items take 6 seconds and so on. An example of a this algorithm is one that recursively calculates fibonacci numbers.

O(N^2) = O(N^2) represents an algorithm that is directly proportional to the square of the sizes of the inputs and must performs N^2 calculations (by definition). Bubblesort is a good example of this algorithm.

O(N log N) = represents an algorithm that will in increase in execution time proportionate to the number of the input times the logarithm of the number of the input. Mergesort and quicksort are good examples of this algorithm.

![Big-O Complexity Chart](/../master/images/bigocomplexitychart.png?raw=true "Big-O Complexity Chart")
![Common Data Structure Operations](/../master/images/commonDataStructureOperations.png??raw=true "Common Data Structure Operations")
![Array Sorting Algorithms](/../master/images/arraySortingAlgos.png?raw=true "Array Sorting Algorithms")
![Big-O-Cheatsheet](/../master/images/big-o-cheat-sheet-poster.png?raw=true "Big-o-cheatsheet")

The Telephone Book

The next best example I can think of is the telephone book, normally called the White Pages or similar but it'll vary from country to country. But I'm talking about the one that lists people by surname and then initials or first name, possibly address and then telephone numbers.

Now if you were instructing a computer to look up the phone number for "John Smith" in a telephone book that contains 1,000,000 names, what would you do? Ignoring the fact that you could guess how far in the S's started (let's assume you can't), what would you do?

A typical implementation might be to open up to the middle, take the 500,000th and compare it to "Smith". If it happens to be "Smith, John", we just got real lucky. Far more likely is that "John Smith" will be before or after that name. If it's after we then divide the last half of the phone book in half and repeat. If it's before then we divide the first half of the phone book in half and repeat. And so on.

This is called a binary search and is used every day in programming whether you realize it or not.

So if you want to find a name in a phone book of a million names you can actually find any name by doing this at most 20 times. In comparing search algorithms we decide that this comparison is our 'n'.

For a phone book of 3 names it takes 2 comparisons (at most).
For 7 it takes at most 3.
For 15 it takes 4.
…
For 1,000,000 it takes 20.
That is staggeringly good isn't it?

In Big-O terms this is O(log n) or logarithmic complexity. Now the logarithm in question could be ln (base e), log10, log2 or some other base. It doesn't matter it's still O(log n) just like O(2n2) and O(100n2) are still both O(n2).

It's worthwhile at this point to explain that Big O can be used to determine three cases with an algorithm:

Best Case: In the telephone book search, the best case is that we find the name in one comparison. This is O(1) or constant complexity;
Expected Case: As discussed above this is O(log n); and
Worst Case: This is also O(log n).
Normally we don't care about the best case. We're interested in the expected and worst case. Sometimes one or the other of these will be more important.

Back to the telephone book.

What if you have a phone number and want to find a name? The police have a reverse phone book but such look-ups are denied to the general public. Or are they? Technically you can reverse look-up a number in an ordinary phone book. How?

You start at the first name and compare the number. If it's a match, great, if not, you move on to the next. You have to do it this way because the phone book is unordered (by phone number anyway).

So to find a name given the phone number (reverse lookup):

Best Case: O(1);
Expected Case: O(n) (for 500,000); and
Worst Case: O(n) (for 1,000,000).
The Travelling Salesman

This is quite a famous problem in computer science and deserves a mention. In this problem you have N towns. Each of those towns is linked to 1 or more other towns by a road of a certain distance. The Travelling Salesman problem is to find the shortest tour that visits every town.

Sounds simple? Think again.

If you have 3 towns A, B and C with roads between all pairs then you could go:

A → B → C
A → C → B
B → C → A
B → A → C
C → A → B
C → B → A
Well actually there's less than that because some of these are equivalent (A → B → C and C → B → A are equivalent, for example, because they use the same roads, just in reverse).

In actuality there are 3 possibilities.

Take this to 4 towns and you have (iirc) 12 possibilities.
With 5 it's 60.
6 becomes 360.
This is a function of a mathematical operation called a factorial. Basically:

5! = 5 × 4 × 3 × 2 × 1 = 120
6! = 6 × 5 × 4 × 3 × 2 × 1 = 720
7! = 7 × 6 × 5 × 4 × 3 × 2 × 1 = 5040
…
25! = 25 × 24 × … × 2 × 1 = 15,511,210,043,330,985,984,000,000
…
50! = 50 × 49 × … × 2 × 1 = 3.04140932 × 1064
So the Big-O of the Travelling Salesman problem is O(n!) or factorial or combinatorial complexity.

By the time you get to 200 towns there isn't enough time left in the universe to solve the problem with traditional computers.

Something to think about.

Polynomial Time

Another point I wanted to make quick mention of is that any algorithm that has a complexity of O(na) is said to have polynomial complexity or is solvable in polynomial time.

O(n), O(n2) etc are all polynomial time. Some problems cannot be solved in polynomial time. Certain things are used in the world because of this. Public Key Cryptography is a prime example. It is computationally hard to find two prime factors of a very large number. If it wasn't, we couldn't use the public key systems we use.

Law of Addition for big-O notation

 O(f(n)) + O(g(n)) is O( f(n) + g(n) )

That is, we when adding complexity classes we bring the two complexity classes
inside the O(...). Ultimately, O( f(n) + g(n) ) results in the bigger of the two
complexity class (because we drop the lower added term). So,

O(N) + O(Log N)  =  O(N + Log N)  =  O(N)

because N is the faster growing function.

This rule helps us understand how to compute the complexity of doing some 
SEQUENCE of operations: executing a statement that is O(f(n)) followed by
executing a statement that is O(g(n)). Executing both statements SEQUENTAILLY
is O(f(n)) + O(g(n)) which is O( f(n) + g(n) ) by the rule above.

For example, if some function call f(...) is O(N) and another function call
g(...) is O(N Log N), then doing the sequence

   f(...)
   g(...)

is O(N) + O(N Log N) = O(N + N Log N) = O(N Log N). Of course, executing the
sequence (calling f twice)

  f(...)
  f(...)

is O(N) + O(N) which is O(N + N) which is O(2N) which is O(N).

Note that for an if statment like

  if test:    	 assume complexity of test is O(T)
     block 1     assume complexity of block 1 is O(B1)
  else:
     block 2     assume complexity of block 2 is O(B2)

The complexity class for the if is O(T) + max(O(B1),O(B2)). The test is always
evaluated, and one of the blocks is always executed. In the worst case, the if
will execute the block with the largest complexity. So, given

  if test:    	 complexity is O(N)
     block 1     complexity is O(N**2)
  else:
     block 2     complexity is O(N)

The complexity class for the if is O(N) + max (O(N**2),O(N))) = O(N) + O(N**2) =
O(N + N**2) = O(N**2). If the test had complexity class O(N**3), then the
complexity class for the if is O(N**3) + max (O(N**2),O(N))) = 
O(N**3) + O(N**2) = O(N**3 + N**2) = O(N**3).

------------------------------------------------------------------------------

Law of Multiplcation for big-O notation

 O(f(n)) * O(g(n)) is O( f(n) * g(n) )

If we repeat an O(f(N)) process O(N) times, the resulting complexity is
O(N)*O(f(N)) = O( Nf(N) ). An example of this is, if some function call f(...)
is O(N**2), then executing that call N times (in the following loop)

  for i in range(N):
    f(...)

is O(N)*O(N**2) = O(N*N**2) = O(N**3)

This rule helps us understand how to compute the complexity of doing some 
statement INSIDE A BLOCK controlled by a statement that is REPEATING it. We
multiply the complexity class of the number of repetitions by the complexity
class of the statement(s) being repeated.

Compound statements can be analyzed by composing the complexity classes of
their constituent statements. For sequential statements the complexity classes
are added; for statements repeated in a loop the complexity classes are
multiplied.

Let's use the data and tools discussed above to analyze (determine their
complexity classes) three different functions that each compute the same
result: whether or not a list contains only unique values (no duplicates). We
will assume in all three examples that len(alist) is N.

1) Algorithm 1: A list is unique if each value in the list does not occur in any
later indexes: alist[i+1:] is a list containing all values after the one at
index i.

def is_unique1 (alist : [int]) -> bool:
    for i in range(len(alist)):		O(N)
        if alist[i] in alist[i+1:]:	O(N) - index+add+slice+in: O(1)+O(1)+O(N)+O(N) = O(N)
            return False		O(1) - never executed in worst case
    return True				O(1)

The complexity class for executing the entire function is O(N) * O(N) + O(1)
= O(N**2). So we know from the previous lecture that if we double the length of
alist, this function takes 4 times as long to execute.

Note that in the worst case, we never return False and keep executing the loop,
so this O(1) does not appear in the answer. Also, in the worst case the list
slice is aliset[1:] which is O(N-1) = O(N).

2) Algorithm 2: A list is unique if when we sort its values, no ADJACENT values
are equal. If there were duplicate values, sorting the list would put these
duplicate values right next to each other (adjacent). Here we copy the list so
as to not mutate (change the order of the parameter's list) by sorting it:
it turns out that copying the list does not increase the complexity class of
the method.

def is_unique2 (alist : [int]) -> bool:
    copy = list(alist)			O(N)
    copy.sort()				O(N Log N) - for fast Python sorting
    for i in range(len(alist)-1):	O(N) - really N-1, but that is O(N)
        if copy[i] == copy[i+1]:	O(1): +, 2 [i],and  == ints: all O(1)
            return False		O(1) - never executed in worst case
    return True	   			O(1)

The complexity class for executing the entire function is given by the sum
O(N) + O(N Log N) + O(N)*O(1) + O(1) = O(N + N Log N + O(N*1) + 1) =
O(N + N Log N + N + 1) = O(N Log N + 2N + 1) = O(N Log N). So the
complexity class for this algorithm/function is lower than the first algorithm,
the is_unique1 function. For large N unque2 will eventually be faster.

Notice that the complexity class for sorting is dominant in this code: it does
most of the work. If we double the length of alist, this function takes a bit
more than twice the amount of time. In N Log N: N doubles and Log N gets a tiny
bit bigger (i.e., Log 2N = 1 + Log N; e.g., Log 2000 = 1 + Log 1000 = 11, so
compared to 1000 Log 1000, 2000 Log 2000 got 2.2 times bigger, or 10% bigger
than just doubling).

Looked at another way if T(N) = c*(N Log N), then T(2N) = c*(2N Log 2N) =
c*2N Log N + c*2N = 2*T(N) + c*2N. Or, computing the doubling signature

T(2N)    c*2(N Log N) + c*2N            2
----- =  -------------------  =  2 + -------
T(N)          c*(N Log N)             Log N

So, the ratio is 2 + a bit (and that bit gets smaller as N increases)

3) Algorithm 3: A list is unique if when we turn it into a set, its length is
unchanged: if duplicate values were added to the set, its length would be
smaller than the length of the list by exactly the number of duplicates in the
list added to the set.

def is_unique3 (alist : [int]) -> bool:
    aset = set(alist)			O(N): construct set from alist values
    return len(aset) == len(alist)	O(1): 2 len (each O(1)) and == ints O(1)

The complexity class for executing the entire function is O(N) + O(1) =
O(N + 1) = O(N). So the complexity class for this algortihm/function is lower
than both the first and second algorithms/functions. If we double the length of
alist, this function takes just twice the amount of time. We could write the
body of this function more simply as: return len(set(alist)) == len(alist),
where evaluating set(alist) takes O(N) and then computing the two len's and
comparing them for equality are all O(1).

So the bottom line here is that there might be many algorithms/functions to
solve some problem. If they are small, we can analyze them statically (looking
at the code, not running it) to determine their complexity classes. For large
problem sizes, the algorithm/function with the smallest complexity class will
be best. For small problem sizes, complexity classes don't determine which is
best (we need to account for the constants and lower order terms when sizes are
small), but we could run the functions (dynamic analysis, aka emperical
analysis) to test which is fastest on small size.

* https://www.topcoder.com/community/data-science/data-science-tutorials/computational-complexity-section-1/



## 4.) Coding (pick you language, C++ idealy im going to pick python)

###read the following
* Programming Interviews Exposed; Secrets to landing your next job by John Monagan and Noah Suojanen (Wiley Computer Publishing)
http://www.wiley.com/WileyCDA/WileyTitle/productCd-047012167X.html

## 5. systems
* system design:  http://research.google.com/pubs/DistributedSystemsandParallelComputing.html
* google file system: http://research.google.com/archive/gfs.html

* google bigtable:  http://research.google.com/archive/bigtable.html

* Google MapReduce: http://research.google.com/archive/mapreduce.html

## 6. Sorting
* know how to sort, bubble-sort least important but know it
* Know all the ni\*log(n) sorting algorithm
* know these for sure:quicksort and merge sort
* know why Merge sort can be highly useful in situations 
* know where quicksort is impractical.

python examples:

#### quicksort:
Quicksort is a very efficient sorting algorithm invented by C.A.R. Hoare. It has two phases:

the partition phase
the sort phase
Most of the work is done in the partition phase - it works out where to divide the work. The sort phase simply sorts the two smaller problems that are generated in the partition phase.

![Quick Sort](/../master/images/quicksort.png?raw=true "Quick sort ex")

This makes Quicksort a good example of the divide and conquer strategy for solving problems. This is similar in principle to the binary search. In the quicksort, we divide the array of items to be sorted into two partitions and then call the quicksort procedure recursively to sort the two partitions, ie we divide the problem into two smaller ones and conquer by solving the smaller ones.

http://www.csanimated.com/animation.php?t=Quicksort

```python
  def quicksort(myList, start, end):
    if start < end:
        # partition the list
        pivot = partition(myList, start, end)
        # sort both halves
        quicksort(myList, start, pivot-1)
        quicksort(myList, pivot+1, end)
    return myList

  def partition(myList, start, end):
    pivot = myList[start]
    left = start+1
    right = end
    done = False
    while not done:
        while left <= right and myList[left] <= pivot:
            left = left + 1
        while myList[right] >= pivot and right >=left:
            right = right -1
        if right < left:
            done= True
        else:
            # swap places
            temp=myList[left]
            myList[left]=myList[right]
            myList[right]=temp
    # swap start with myList[right]
    temp=myList[start]
    myList[start]=myList[right]
    myList[right]=temp
    return right
```

#### mergesort:
Merge sort is a sorting technique based on divide and conquer technique. With worst-case time complexity being Ο(n log n), it is one of the most respected algorithms.

https://www.youtube.com/watch?v=GCae1WNvnZM

Merge sort first divides the array into equal halves and then combines them in a sorted manner.

![Merge Sort](/../master/images/mergesort1.png?raw=true "Merge sort ex")
![Merge Sort](/../master/images/mergesort2.png?raw=true "Merge sort continued ex")

Merge sort keeps on dividing the list into equal halves until it can no more be divided. By definition, if it is only one element in the list, it is sorted. Then, merge sort combines the smaller sorted lists keeping the new list sorted too.

Step 1 − if it is only one element in the list it is already sorted, return.
Step 2 − divide the list recursively into two halves until it can no more be divided.
Step 3 − merge the smaller lists into new list in sorted order.

Pseudocode
We shall now see the pseudocodes for merge sort functions. As our algorithms point out two main functions − divide & merge.
Merge sort works with recursion and we shall see our implementation in the same way.

procedure mergesort( var a as array )
   if ( n == 1 ) return a

   var l1 as array = a[0] ... a[n/2]
   var l2 as array = a[n/2+1] ... a[n]

   l1 = mergesort( l1 )
   l2 = mergesort( l2 )

   return merge( l1, l2 )
end procedure

procedure merge( var a as array, var b as array )

   var c as array

   while ( a and b have elements )
      if ( a[0] > b[0] )
         add b[0] to the end of c
         remove b[0] from b
      else
         add a[0] to the end of c
         remove a[0] from a
      end if
   end while
   
   while ( a has elements )
      add a[0] to the end of c
      remove a[0] from a
   end while
   
   while ( b has elements )
      add b[0] to the end of c
      remove b[0] from b
   end while
   
   return c
	
end procedure

```python 
def mergeSort(alist):
    print("Splitting ",alist)
    if len(alist)>1:
        mid = len(alist)//2
        lefthalf = alist[:mid]
        righthalf = alist[mid:]

        mergeSort(lefthalf)
        mergeSort(righthalf)

        i=0
        j=0
        k=0
        while i < len(lefthalf) and j < len(righthalf):
            if lefthalf[i] < righthalf[j]:
                alist[k]=lefthalf[i]
                i=i+1
            else:
                alist[k]=righthalf[j]
                j=j+1
            k=k+1

        while i < len(lefthalf):
            alist[k]=lefthalf[i]
            i=i+1
            k=k+1

        while j < len(righthalf):
            alist[k]=righthalf[j]
            j=j+1
            k=k+1
    print("Merging ",alist)

alist = [54,26,93,17,77,31,44,55,20]
mergeSort(alist)
print(alist)

```

#### tim sort:
Timsort is a hybrid algorithm combining merge and insertion sorts. It was invented in 2002 by Tim Peters for use in the Python programming language.

Timsort begins by looking for small runs (called miniruns) of data that is already sorted (either small to large or vice versa). If no runs of a long-enough length (minirun is short for “minimum run”) are found then an insertion step takes place to create them. These miniruns are sorted using an insertion sort as explained above, and then combined with each other using Mergesort, again as explained above. The trick of Timsort is how it selects and creates miniruns,

![Tim Sort](/../master/images/timsort1.png?raw=true "Tim sort info")

![Tim Sort ...](/../master/images/timsort2.png?raw=true "Tim sort continued")

"""
|-----------------------------------------------------------|
|                         Tim Sort                          |
|-----------------------------------------------------------|
|Created By Tim Roberts      ||  Python's Builtin Sort      |
|Worst case performance      ||  O(n log n)                 |
|Best case performance       ||  O(n)                       |
|Average case performance    ||  O(n log n)                 |
|Worst case space complexity ||  O(n)                       |
|-----------------------------------------------------------|
"""

```python 
def tim_sort(array): 
	return sorted(array"
```

#### heapsort:
heaps are based on the notion of complete tree
2 main steps are
creation of heap
processing of heap

creation of heap = put the largest element on the top in each step size of the Heap increase
put the elements in heap as they occur in swquential order i.e, parent then leftchild and then right child.
Each time (of inserting a new node/child) compare it with its Parent Node
Is? Child Node (left or Right ) is less than or equal or greater than or equal to that of the parent node ...
If it is greater than its successor than interchange them. 

processing of the heap:
The last element of last level should be replsced by ztop element of the list.
zin this process the largest element will be at last place
List weill be sdorted out in increasing order from root to leaf
After reolacing the top element Creatuion of the Heap takes place 
In each stepo size of Heap decreased

![Heap Sort](/../master/images/heapsort0.png?raw=true "heap sort ex")
![Heap Sort](/../master/images/heapsort1.png?raw=true "heap sort continued")
![Heap Sort](/../master/images/heapsort2.png?raw=true "heap sort continued")
![Heap Sort](/../master/images/heapsort3.png?raw=true "heap sort continued")
![Heap Sort](/../master/images/heapsort4.png?raw=true "heap sort continued")
![Heap Sort](/../master/images/heapsort5.png?raw=true "heap sort continued")
![Heap Sort](/../master/images/heapsort6.png?raw=true "heap sort continued")

https://www.youtube.com/watch?v=onlhnHpGgC4

```python
#  Statement:
#  Given a disordered list of integers (or any other items),
#  rearrange the integers in natural order.
#
#  Sample Input: [8,5,3,1,9,6,0,7,4,2,5]
#  Sample Output: [0,1,2,3,4,5,5,6,7,8,9]
#
#  Time Complexity of Solution:
#  Best O(nlog(n)); Average O(nlog(n)); Worst O(nlog(n)).
#
#  Approach:
#  Heap sort happens in two phases. In the first phase, the array
#  is transformed into a heap. A heap is a binary tree where
#  1) each node is greater than each of its children
#  2) the tree is perfectly balanced
#  3) all leaves are in the leftmost position available.
#  In phase two the heap is continuously reduced to a sorted array:
#  1) while the heap is not empty
#  - remove the top of the head into an array
#  - fix the heap.
#  Heap sort was invented by John Williams not by B. R. Heap.
#
#  MoveDown:
#  The movedown method checks and verifies that the structure is a heap.
#
#  Technical Details:
#  A heap is based on an array just as a hashmap is based on an
#  array. For a heap, the children of an element n are at index
#  2n+1 for the left child and 2n+2 for the right child.
#
#  The movedown function checks that an element is greater than its
#  children. If not the values of element and child are swapped. The
#  function continues to check and swap until the element is at a
#  position where it is greater than its children.
#======================================================================= 
 def heapsort( aList ):
  # convert aList to heap
  length = len( aList ) - 1
  leastParent = length / 2
  for i in range ( leastParent, -1, -1 ):
    moveDown( aList, i, length )
 
  # flatten heap into sorted array
  for i in range ( length, 0, -1 ):
    if aList[0] > aList[i]:
      swap( aList, 0, i )
      moveDown( aList, 0, i - 1 )
 
def moveDown( aList, first, last ):
  largest = 2 * first + 1
  while largest <= last:
    # right child exists and is larger than left child
    if ( largest < last ) and ( aList[largest] < aList[largest + 1] ):
      largest += 1
 
    # right child is larger than parent
    if aList[largest] > aList[first]:
      swap( aList, largest, first )
      # move down to largest child
      first = largest;
      largest = 2 * first + 1
    else:
      return # force exit
  
def swap( A, x, y ):
  tmp = A[x]
  A[x] = A[y]
  A[y] = tmp
```

buble sort:
	Bubble sort is one of the most basic sorting algorithm that is the simplest to understand. It’s basic idea is to bubble up the largest(or smallest), then the 2nd largest and the the 3rd and so on to the end of the list. Each bubble up takes a full sweep through the list

https://www.youtube.com/watch?v=P00xJgWzz2c

![Bubble Sort](/../master/images/bubblesort.png?raw=true "Bubble sort ex")

```python 
def bubble_sort(items):
        """ Implementation of bubble sort """
        for i in range(len(items)):
                for j in range(len(items)-1-i):
                        if items[j] &gt; items[j+1]:
                                items[j], items[j+1] = items[j+1], items[j]     # Swap!
 
```

insertion sort:
The insertion sort uses the principle of a marker moving along a list with a sorted side to the left side of the marker and the unsorted side to the right of the marker.

![Insertion sort](/../master/images/insertionsort.png?raw=true "Insertion sort ex")

http://courses.cs.vt.edu/csonline/Algorithms/Lessons/InsertionCardSort/insertioncardsort.html
https://www.youtube.com/watch?v=Nkw6Jg_Gi4w

```python 
def insertionSort(alist):
   for index in range(1,len(alist)):

     currentvalue = alist[index]
     position = index

     while position>0 and alist[position-1]>currentvalue:
         alist[position]=alist[position-1]
         position = position-1

     alist[position]=currentvalue

alist = [54,26,93,17,77,31,44,55,20]
insertionSort(alist)
print(alist)
```

selection sort:
The selection sort improves on the bubble sort by making only one exchange for every pass through the list. In order to do this, a selection sort looks for the largest value as it makes a pass and, after completing the pass, places it in the proper location. As with a bubble sort, after the first pass, the largest item is in the correct place. After the second pass, the next largest is in place. This process continues and requires n−1n−1 passes to sort n items, since the final item must be in place after the (n−1)(n−1) st pass.


![Selection Sort](/../master/images/selectionsort.png?raw=true "Selection sort ex")

https://www.youtube.com/watch?v=6nDMgr0-Yyo

```python 
def selectionSort(alist):
   for fillslot in range(len(alist)-1,0,-1):
       positionOfMax=0
       for location in range(1,fillslot+1):
           if alist[location]>alist[positionOfMax]:
               positionOfMax = location

       temp = alist[fillslot]
       alist[fillslot] = alist[positionOfMax]
       alist[positionOfMax] = temp

alist = [54,26,93,17,77,31,44,55,20]
selectionSort(alist)
print(alist)
```

tree sort:
Tree sort is a sorting algorithm that is based on Binary Search Tree data structure. It first creates a binary search tree from the elements of the input list or array and then performs an in-order traversal on the created binary search tree to get the elements in sorted order.

![Tree Sort](/../master/images/treesort0.png?raw=true "tree sort ex")
![Tree Sort...](/../master/images/treesort1.png?raw=true "tree sort continued")
![Tree Sort...](/../master/images/treesort2.png?raw=true "tree sort continued")
![Tree Sort...](/../master/images/treesort3.png?raw=true "tree sort continued")

https://www.youtube.com/watch?v=pYT9F8_LFTM

Algorithm:

Step 1: Take the elements input in an array.
Step 2: Create a Binary search tree by inserting data items from the array into the
        binary searh tree.
Step 3: Perform in-order traversal on the tree to get the elements in sorted order.

```python 
   class Node:
      def __init__(self,info): #constructor of class
          self.info = info  #information for node
          self.left = None  #left leef
          self.right = None #right leef
          self.level = None #level none defined
      def __str__(self):
          return str(self.info) #return as string

class searchtree:
      def __init__(self): #constructor of class
          self.root = None

      def create(self,val):  #create binary search tree nodes
          if self.root == None:
             self.root = Node(val)
          else:
             current = self.root
             while 1:
                 if val < current.info:
                   if current.left:
                      current = current.left
                   else:
                      current.left = Node(val)
                      break;      

                 elif val > current.info:
                    if current.right:
                       current = current.right
                    else:
                       current.right = Node(val)
                       break;      
                 else:
                    break 

      def bft(self): #Breadth-First Traversal
          self.root.level = 0 
          queue = [self.root]
          out = []
          current_level = self.root.level
          while len(queue) > 0:
             current_node = queue.pop(0)
             if current_node.level > current_level:
                current_level += 1
                out.append("\n")
             out.append(str(current_node.info) + " ")
             if current_node.left:
                current_node.left.level = current_level + 1
                queue.append(current_node.left)  
             if current_node.right:
                current_node.right.level = current_level + 1
                queue.append(current_node.right)
             print "".join(out)   

      def inorder(self,node):
           if node is not None:              
              self.inorder(node.left)
              print node.info
              self.inorder(node.right)

      def preorder(self,node):
           if node is not None:
              print node.info
              self.preorder(node.left)
              self.preorder(node.right)

      def postorder(self,node):
           if node is not None:
              self.postorder(node.left)
              self.postorder(node.right)
              print node.info

tree = searchtree()     
arr = [8,3,1,6,4,7,10,14,13]
for i in arr:
    tree.create(i)
print 'Breadth-First Traversal'
tree.bft()
print 'Inorder Traversal'
tree.inorder(tree.root) 
print 'Preorder Traversal'
tree.preorder(tree.root) 
print 'Postorder Traversal'
tree.postorder(tree.root) 
```

shell sort:
"""
|-----------------------------------------------------------|
|                        Shell Sort                         |
|-----------------------------------------------------------|
|Type                        ||  In-place comparison sort   |
|Worst case performance      ||  O(n2)                      |
|Best case performance       ||  O(n log2 n)                |
|Average case performance    ||  depends on gap sequence    |
|Worst case space complexity ||  O(n) total, O(1) auxiliary |
|-----------------------------------------------------------|
"""


![Shell Sort](/../master/images/shellsort.png?raw=true "shell sort ex")
https://www.youtube.com/watch?v=M9YCh-ZeC7Y

```python
def shell_sort(array):
    mid = len(array) / 2
    while mid:
        for i in range(len(array)):
            j = i
            temp = array[i]
            while j >= mid and array[j-mid] > temp:
                array[j] = array[j - mid]
                j -= mid
            array[j] = temp
        mid = mid/2 if mid/2 else (0 if mid == 1 else 1)
    return array
```

bucket sort:
Bucket sort can be exceptionally fast because of the way elements are assigned to buckets, typically using an array where the index is the value. This means that more auxiliary memory is required for the buckets at the cost of running time than more comparison sorts. It runs in O(n+k)O(n+k) time in the average case where nn is the number of elements to be sorted and kk is the number of buckets.

![Bucket Sort](/../master/images/bucketsort.png?raw=true "bucket sort ex")
![Bucket Sort Complexity](/../master/images/bucketsortcomplexity.png?raw=true "bucket sort complexity")

when its fast:
Bucket sort’s best case occurs when the data being sorted can be distributed between the buckets perfectly. If the values are sparsely allocated over the possible value range, a larger bucket size is better since the buckets will likely be more evenly distributed. An example of this is [2303, 33, 1044], if buckets can only contain 5 different values then for this example 461 buckets would need to be initialised. A bucket size of 200-1000 would be much more reasonable.
The inverse of this is also true; a densely allocated array like [103, 99, 119, 112, 111] performs best when buckets are as small as possible.
Bucket sort is an ideal algorithm choice when:
The additional O(n + k)O(n+k) memory usage is not an issue
Elements are expected to be fairly evenly distributed

when its slow:
Bucket sort performs at its worst, O(n^2), when all elements at allocated to the same bucket. Since individual buckets are sorted using another algorithm, if only a single bucket needs to be sorted, bucket sort will take on the complexity of the inner sorting algorithm.
This depends on the individual implementation though and can be mitigated. For example a bucket sort algorithm could be made to work with large bucket sizes by using insertion sort on small buckets (due to its low overhead), and merge sort or quicksort on larger buckets.

```python 
def sort(array, bucketSize=DEFAULT_BUCKET_SIZE):
  if len(array) == 0:
    return array

  # Determine minimum and maximum values
  minValue = array[0]
  maxValue = array[0]
  for i in range(1, len(array)):
    if array[i] < minValue:
      minValue = array[i]
    elif array[i] > maxValue:
      maxValue = array[i]

  # Initialize buckets
  bucketCount = math.floor((maxValue - minValue) / bucketSize) + 1
  buckets = []
  for i in range(0, bucketCount):
    buckets.append([])

  # Distribute input array values into buckets
  for i in range(0, len(array)):
    buckets[math.floor((array[i] - minValue) / bucketSize)].append(array[i])

  # Sort buckets and place back into input array
  array = []
  for i in range(0, len(buckets)):
    insertion_sort.sort(buckets[i])
    for j in range(0, len(buckets[i])):
      array.append(buckets[i][j])

  return array
  ```
radix sort:
The algorithm is named radix sort as it specifies the radix rr to be used which changes how the sort is performed. The radix, or base, of the number system is the number of digits that represent a single position in the number; a radix of 2 is binary (0-1), 10 is decimal (0-9), 16 is hexadecimal (0-F) and so on. Since the radix determines the number of buckets in addition to the word size ww used in the algorithm, changing it can drastically change how the sort plays out:

https://www.youtube.com/watch?v=YXFI4osELGU

![Radix Sort](/../master/images/radixsort1.png?raw=true "radix sort ex")
![Radix Sort](/../master/images/radixsort2.png?raw=true "radix sort ex")
![Radix Sort](/../master/images/radixsort3.png?raw=true "radix sort ex")
![Radix Sort](/../master/images/radixsort4.png?raw=true "radix sort ex")
![Radix Sort](/../master/images/radixsort5.png?raw=true "radix sort ex")
![Radix Sort](/../master/images/radixsort6.png?raw=true "radix sort ex")
![Radix Sort](/../master/images/radixsort7.png?raw=true "radix sort ex")
![Radix Sort](/../master/images/radixsort8.png?raw=true "radix sort ex")
![Radix Sort](/../master/images/radixsort9.png?raw=true "radix sort ex")
![Radix Sort](/../master/images/radixsort10.png?raw=true "radix sort ex")
![Radix Sort](/../master/images/radixsort11.png?raw=true "radix sort ex")
![Radix Sort](/../master/images/radixsort12.png?raw=true "radix sort ex")
![Radix Sort](/../master/images/radixsort13.png?raw=true "radix sort ex")

fast: 
Since comparison sorts cannot perform better than O(n\log n)O(nlogn), LSD radix sort is considered one of the best alternatives provided the word size ww is expected to be less than \log nlogn.
It does however have limitations on the type of keys that can be sorted in that they need to have some way of being split up (ie. the radix), so it’s typically only used for string (where r=255r=255 for ASCII characters) and integer keys.

slow:
Radix sort is slowest when the word size is large, such as when there is a large key range but small radix. The reason that a large radix is not always used is because then it essentially becomes counting sort, with the large memory footprint associated with it.

```python
def sort(array, radix=10):
  if len(array) == 0:
    return array

  # Determine minimum and maximum values
  minValue = array[0];
  maxValue = array[0];
  for i in range(1, len(array)):
    if array[i] < minValue:
      minValue = array[i]
    elif array[i] > maxValue:
      maxValue = array[i]

  # Perform counting sort on each exponent/digit, starting at the least
  # significant digit
  exponent = 1
  while (maxValue - minValue) / exponent >= 1:
    array = countingSortByDigit(array, radix, exponent, minValue)
    exponent *= radix

  return array

def countingSortByDigit(array, radix, exponent, minValue):
  bucketIndex = -1
  buckets = [0] * radix
  output = [None] * len(array)

  # Count frequencies
  for i in range(0, len(array)):
    bucketIndex = math.floor(((array[i] - minValue) / exponent) % radix)
    buckets[bucketIndex] += 1

  # Compute cumulates
  for i in range(1, radix):
    buckets[i] += buckets[i - 1]

  # Move records
  for i in range(len(array) - 1, -1, -1):
    bucketIndex = math.floor(((array[i] - minValue) / exponent) % radix)
    buckets[bucketIndex] -= 1
    output[buckets[bucketIndex]] = array[i]

  return output
```

counting sort:
	is a sorting technique based on keys between a specific range
	it works by counting the number of objects having distinct key values
	Then doing some arithmetic to calculate the position of each object in the output sequence
	
	Time Complexity: O(n+k) where n is the number of elements in input array and k is the range of input.
Auxiliary Space: O(n+k)

Points to be noted:
Counting sort is efficient if the range of input data is not significantly greater than the number of objects to be sorted. Consider the situation where the input sequence is between range 1 to 10K and the data is 10, 5, 10K, 5K.
It is not a comparison based sorting. It running time complexity is O(n) with space proportional to the range of data.
It is often used as a sub-routine to another sorting algorithm like radix sort.
Counting sort uses a partial hashing to count the occurrence of the data object in O(1).
Counting sort can be extended to work for negative inputs also.
	
https://www.youtube.com/watch?v=7zuGmKfUt7s
	
![Counting Sort](/../master/images/countingsort1.png?raw=true "counting sort ex")	
![Counting Sort](/../master/images/countingsort2.png?raw=true "counting sort ex")
![Counting Sort](/../master/images/countingsort3.png?raw=true "counting sort ex")
![Counting Sort](/../master/images/countingsort4.png?raw=true "counting sort ex")
![Counting Sort](/../master/images/countingsort5.png?raw=true "counting sort ex")
![Counting Sort](/../master/images/countingsort6.png?raw=true "counting sort ex")
![Counting Sort](/../master/images/countingsort7.png?raw=true "counting sort ex")
![Counting Sort](/../master/images/countingsort8.png?raw=true "counting sort ex")
![Counting Sort](/../master/images/countingsort9.png?raw=true "counting sort ex")
![Counting Sort](/../master/images/countingsort10.png?raw=true "counting sort ex")
![Counting Sort](/../master/images/countingsort11.png?raw=true "counting sort ex")
![Counting Sort](/../master/images/countingsort12.png?raw=true "counting sort ex")

```python
def counting_sort(array, maxval):
    """in-place counting sort"""
    m = maxval + 1
    count = [0] * m               # init with zeros
    for a in array:
        count[a] += 1             # count occurences
    i = 0
    for a in range(m):            # emit
        for c in range(count[a]): # - emit 'count[a]' copies of 'a'
            array[i] = a
            i += 1
    return (array,count)

print counting_sort( [1, 4, 7, 2, 1, 3, 2, 1, 4, 2, 3, 2, 1], 7 )
#            prints: [1, 1, 1, 1, 2, 2, 2, 2, 3, 3, 4, 4, 7],[0, 4, 4, 2, 2, 0, 0, 1]
```

cubesort sort:


## 7. hashtables (must know or will fail)
* Be able to implement one using only arrays in your favorite language, in about the space of one interview.
python example:

hash Table:

## 8. Trees
*  basic tree construction, traversal and manipulation algorithms.
* Familiarize yourself with binary trees, n-ary trees, and trie-trees
* Be familiar with at least one type of balanced binary tree, whether it's a red/black tree, a splay tree or an AVL tree, and know how it's implemented
* Understand tree traversal algorithms: BFS and DFS, and know the difference between inorder, postorder and preorder.

python examples:

binary search Tree:

cartesian Tree:

B-tree:

Red-Black Tree:

Splay Tree:

AVL tree:

KD tree:

## 9. Graphs
* 3 basic ways to represent a graph in memory (objects and pointers, matrix, and adjacency list); familiarize yourself with each representation and its pros & cons
* You should know the basic graph traversal algorithms: breadth-first search and depth-first search
* Know their computational complexity, their tradeoffs, and how to implement them in real code
* study up on fancier algorithms, such as Dijkstra and A\*.

## 10. Other data structures
* know about the most famous classes of NP-complete problems, such as traveling salesman and the knapsack problem, and be able to recognize them when an interviewer asks you them in disguise.
* Find out what NP-complete means

## 11 Mathmatics
* Spend some time before the interview refreshing your memory on (or teaching yourself) the essentials of combinatorics and probability. You should be familiar with n-choose-k problems and their ilk – the more the better.

## 12 Operating Syatems
* Know about processes, threads and concurrency issues
* Know about locks and mutexes and semaphores and monitors and how they work
* Know about deadlock and livelock and how to avoid them
* Know what resources a processes needs, and a thread needs, and how context switching works, and how it's initiated by the operating system and underlying hardware
* Know a little about scheduling. 
* The world is rapidly moving towards multi-core, so know the fundamentals of "modern" concurrency constructs.
* resource = http://research.google.com/pubs/DistributedSystemsandParallelComputing.html

## 13 Important reaserch publications:
*  http://research.google.com/pubs/papers.html
* paper on Google’s Hybrid Approach to Research:
http://static.googleusercontent.com/media/research.google.com/en/us/pubs/archive/38149.pdf

## 14 Must reads
* Programming Interviews Exposed: Secrets to Landing Your Next Job by John Mongan and Noah Suojanen
* "Programming Pearls" by Jon Bentley
* "Cormen/Leiserson/Rivest/Stein: Introduction to Algorithms" 

## 15 online resourse
* www.topcoder.com - launch the area widget and then go to the practice rooms where you can play the problem in the  first/second division as a warm up
* projecteuler.net - programming problems you wont normally come across 

## 16 tips for interviewing at google
* https://www.youtube.com/watch?v=w887NIa_V9w

## 17 google products
*  https://www.google.com/intl/en/about/products/

## 18 5 essental Phone screen questions by Steve Yegge(google engineer)
* https://sites.google.com/site/steveyegge2/five-essential-phone-screen-questions

## 19 Types of algorithum question google asks: topCider Tutorials 
* https://www.topcoder.com/community/data-science/data-science-tutorials/

## 20 The Official Google Blog: "Baby steps to a new job" by Gretta Cook(google engineer)

## 21 “How to Get Hired” by Dan Kegel (Google Engineer)
* https://www.youtube.com/watch?v=qc1owf2-220

## 22 "google recruiters share Technical Interview Tips
* https://www.youtube.com/watch?v=qc1owf2-220

## 23 Candidate Coaching Session: Tech Interviewing
*  https://www.youtube.com/watch?v=oWbUtlUhwa8

## 24 Interviewing at Google
* https://www.youtube.com/watch?v=w887NIa_V9w

## 25 extra credit
* 1 - Interview Cake sends you a weekly question  https://www.interviewcake.com
* 2 - Daily practice questions https://leetcode.com/ 
* 3 - Pramp helps with mock interviews   https://www.pramp.com 
* 4 - clear code: A handbook of agile software craftsmanship http://ricardogeek.com/docs/clean_code.pdf

