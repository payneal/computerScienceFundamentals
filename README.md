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

## 7. hashtables (must know or will fail)
* Be able to implement one using only arrays in your favorite language, in about the space of one interview.

## 8. Trees
*  basic tree construction, traversal and manipulation algorithms.
* Familiarize yourself with binary trees, n-ary trees, and trie-trees
* Be familiar with at least one type of balanced binary tree, whether it's a red/black tree, a splay tree or an AVL tree, and know how it's implemented
* Understand tree traversal algorithms: BFS and DFS, and know the difference between inorder, postorder and preorder.

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

