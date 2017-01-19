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

quicksort:
Quicksort is a very efficient sorting algorithm invented by C.A.R. Hoare. It has two phases:

the partition phase
the sort phase
Most of the work is done in the partition phase - it works out where to divide the work. The sort phase simply sorts the two smaller problems that are generated in the partition phase.

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

mergesort:

timsort:

heapsort:

buble sort:

insertion sort:
The insertion sort uses the principle of a marker moving along a list with a sorted side to the left side of the marker and the unsorted side to the right of the marker.

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



bucket sort:

radix sort:

counting sort:

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

