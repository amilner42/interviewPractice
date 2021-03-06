# Technical Interview Preparation Guide
 
### [Introduction]
If you have an interview coming up at a company like Google or Amazon (and many others ...) that you know will ask
technical questions, then you have come to a good place to prepare yourself! Listed in this README are a bunch of 
technical computer science questions that will ALL be answered inside separate packages/class-files. Each solution also 
may include an associated demo file which will contain a main class and demo that solution, it is advised to play around
with these and learn about all the corner cases! 

### [Organization]
1. Data Structures
	* Implement this data structure
	* Implement this method for a data structure
2. Sorts and Searches 
	* Implement this sort
	* Implement this search
3. Interview Problems
	* Solve this problem

### [Training]
It is not organized like this for no reason! It is recommended to have a good understanding of different data structures
and sorts and searches before moving on to general interview problems. These will be your tools to help understand and 
solve different interview problems. Doing all the sorts is optional, but it is recommended that you have a good
understanding of at minimum one O(nlogn) sort.

### [Navigation]
This README was designed to be simple and fast to browse using only control-f. If you quickly want to jump to somewhere 
in the readme, simply search (using control-f) for it in square brackets. Make sure your search is not case sensitive!

Quick Search Options: 
* data-structures: [name-of-data-structure] 
* sorts: [name-of-sort]
* interview problems: [P#]
* section: [name-of-section-header]


### [Contributing] 
If you find any mistakes in my code, and there will be mistakes, try and fix them as an exercise! Once you think you have
a working implementation, shoot me a pull request, I always appreciate friendly help :) If you have any ideas for things
you wanna add, feel free to code it up and shoot me a pull request, just please keep your code clean - clean code or no
code at all. Again I always appreciate help and thanks in advance :) 

## [Data Structures] 

### [QUEUE]
* Implement a Queue of ints using a circular array. Deal with under/overflow using exceptions appropriately. This Queue
must have the following methods:
```java
    public Queue(int maxSize)
    public void enqueue(int data)
    public int dequeue()
    public int peek()
    public boolean isFull()
    public boolean isEmpty()
    public String toString()
```

* Implement a Queue using two stacks, make use of generics. This StackQueue must have the following methods:
```java
    public StackQueue()
    public StackQueue(Type[] list)
    public void enqueue(Type obj)
    public Type dequeue()
    public boolean isEmpty()
```

### [LINKED LIST]
* Implement a LinkedList that can store any type using generics. To make this class, it helps to have a class for Node
that also uses generics to store any type. This LinkedList must have the following methods:
```java
    public LinkedList()
    public Node<Type> find(Type data)
    public int getLength()
    public void addDataAtHead(Type data)
    public void addNodeAtHead(Node<Type> nextNode)
    public Node<Type> deleteHead() throws ...
    public String toString()
```

* Do the exact same as question 2, but use a DoubleLinkedList. You will need a new Node class

* Reverse a SinglyLinkedList, the method header should look like:
```java
    public void reverse() // put this method inside your LinkedList class
```
* Check if a SinglyLinkedList is cyclic, the method header should look like:
```java
    public boolean cyclic() // put this method inside your LinkedList class
```
### [STACK]
* Implement a Stack that can store any type using generics. For the underlying data type, use an ArrayList. What are the
speeds of each of these methods in big-O notation if implemented correctly? It must have the following methods:
```java
    public Stack()
    public Type pop()
    public void push(Type data)
    public Type peek()
    public String toString()
```

### [HEAP]
* Implement a Heap that stores integers. Implement the heap in any way you think is best, but make sure it is fast! What
are the speeds of each of these methods in big-O notation if implemented correctly? It must have the following methods:
```java
    public Heap(int initialSize)
    public Heap(int[] initialValues)
    public void add(int integer) 
    public boolean delete(int integer) 
    public int peek()
    public int pop()
    public boolean contains(int integer)
    public boolean isEmpty()
    public int size()
```
	
### [PRIORITY QUEUE]
* Implement a Priority Queue that stores integers. It must have the following methods:
```java
    public PriorityQueue(int initialSize)
    public PriorityQueue(int [] list)
    public void enqueue(int data)
    public int dequeue()
    public int peek()
    public boolean isEmpty()
```

### [BINARY SEARCH TREE]
* Implement a BST that stores Integers. To make this BST, it will be useful to have a TreeNode as well. For the traversal
methods, simply print out the node data values as you traverse them. This BST must have the following methods:
```java
    public BinarySearchTree(Integer data)
    public BinarySearchTree()
    public TreeNode find(Integer searchKey)
    public void insert(TreeNode insertNode)
    public boolean delete(Integer searchKey)  // return true if object deleted, false if object not in list
    public void inOrderTraversal()
    public void preOrderTraversal()
    public void postOrderTraversal()
    public TreeNode smallest()
    public TreeNode biggest()
```

## [Sorts / Searches] 
### [Sorts]
For all sorts, analyze the speed using Big-O notation. Program all sorts as static methods in individual classes that each
have a main method that tests out the sort

* Implement [Bubble sort], the method header should look like: 
```java
    private static void bubbleSort(int[] list)
```

* Implement [Selection sort], the method header should look like: 
```java
    private static void selectionSort(int[] list)
```

* Implement [Insertion sort], the method header should look like:  
```java
    private static void insertionSort(int[] list)
```

* Implement [Merge sort], the method header should look like: 
```java
    private static void mergeSort(int[] list) 
```

* Implement [Quick Sort], the method header should look like:
```java
    private static void quickSort(int[] list)
```

* Implement [Shell Sort], the method header should look like:
```java
    private static void shellSort(int[] list)
```

* Implement [Counting Sort], the method header should look like:
```java
    private static void countingSort(int[] list , int startRange , int endRange)
```

* Implement [Radix Sort], the method header should look like:
```java
    private static void radixSort(int[] list)
```

* Implement [Bucket Sort], the method header should look like:
```java
    private static void bucketSort(int[] list)
```

* Implement [Heap Sort] (this is a great place to test your own heap), the method header should look like:
```java
    private static void heapSort(int[] list)
```

### [Searches]
* Implement a [binary search] that takes in a sorted array, the method header should look like:
```java
    private static int binarySearchArray(int [] list, int searchKey)
```

## [Interview Problems]
*[P1]*
Implement factorial recursively. Implement it again, but this time use tail recursion. What is tail recursion? Is Java
optimized for tail recursion?

*[P2]*
Solve the famous Towers of Hanoi problem. Is it tail recursive? Why or why not?

*[P3]* 
Assuming I give you an array of numbers, lets say they represent stock prices, find me the most money you could make
that day by buying and selling a single stock. If the stocks go down all day, you should find me the least amount of money
I could lose that day. The method header should look like:
```java
	private static int bestStockTrade(int[] stockPrices) throws ...
``` 

*[P4]* 
Given an array of integers, eg [1 , 2 , 3, 4], return an array where at each index you get the result of multiplying 
by all the other values. Eg. [1 , 2 , 3 , 4] --> [2x3x4 , 1x3x4, 1x2x4 , 1x2x3]. Do NOT use division. The method header 
should look like: 
```java
	private static int[] productAllButMe(int[] data) throws ...
```
  
*[P5]* 
Given an array of integers, what is the maximum product you could get from multiplying any 3 of the integers. The 
method header should look like:
```java
	private static int productOfThree(int[] data) throws ...
```

*[P6]* 
Given an array of pairs of integers, write a function that goes through and see which parts of the timeline
are covered. Eg. Given the array of [(1,4) , (2,7) , (9,11) , (1,3) , (12,14)] --> [(1,7) , (9,14)]. You could 
imagine this being useful if we had a list of everyones schedule and we wanted to see when everyone was free. For the actual
representation of the input, use the following class:
```java
class Schedule {
	public int startTime;
  	public int endTime;

	public Schedule(int startTime , int endTime) {
 		 this.startTime = startTime;
 		 this.endTime = endTime;
	  }

	 @Override
 	 public String toString() {
 	 	return "(" + startTime + " , " + endTime + ")";
 	 }
}
```
For the method header:
```java
	private static List<Schedule> scheduler(List<Schedule> schedules)
```
    
*[P7]*
Given an array of People, where a person is represented by a startTime and finishTime for their work shift, return
the shortest list possible of people where those people see all other people during their shifts. For example, if 
given these people (1 , 2) , (2 , 10) , (5 , 6) then you should return (2 , 10) because this person sees everyone 
else during his shift. If given (1 , 5) , (4 , 10) , (2 , 3) , (11 , 13)  --> (1 , 5) , (11 , 13). For the actual
representation of person, use the following class:
```java
class Person {
	public int startTime;
	public int finishTime;

	public Person(int startTime , int finishTime) {
		this.startTime = startTime;
		this.finishTime = finishTime;
	}

	@Override
	public String toString() {
		return "(" + startTime + " , " + finishTime + ")";
	}
}
```

For the method header:
```java
	private static List<Person> selectPeople(List<Person> people) throws ...
```
    
*[P8]* 
Given an array of integers, where there is guaranteed to be one number that is not duplicated, find that number. Note
that in this list of coupled numbers, only 1 number has no duplicate, and every other number has one and only one 
duplicate. Possible inputs: [1 , 2 , 2 , 3 , 3 , 4 , 4] , [2] , [3 , 7 , 3] etc...
    
For the method header:
```java
	private static int uncoupledInteger(int[] list) 
```
Extra Points: Can you do it in constant memory and linear time? 

*[P9]*
Given a string that is full of delimiters, check whether the string had balanced delimiters. The only delimiters we will
worry about in this problem are the following: [ ] { } ( ). There are no other characters in this string except for the
delimiters. The following strings are balanced and should return true: "" , "()" , "{}()[]" , "([{}])". The following
strings are not balanced and should return false: "[" , "{}}" , "{{]}" , "{[}]"

For the method header: 
```java
	private static boolean balancedDelimiters(String delimiters) 
```

*[P10]*
Given an array of integers and a target sum, make a function that returns true if the target sum is a sum of 
two of the integers in the array. For example, given the array [1 , 2 , 3 , 4, -100 , 0 , 0] and target 5 it should 
return true because 4 + 1 = 5. Note that if the same array was given, but the target was 8, the answer would return false.
You cannot add an integer to itself to produce the target, you must find two separate integers. Note that these two
separate integers could have the same value, eg. if the same array was given but 0 was given as the target, it should return
true because there are two integers in the array that sum to 0 - the 0 in the 5th index and the 0 in the 6th index. 

For the method header: 
```java
	private static boolean targetSummable(int[] array , int target) 
```