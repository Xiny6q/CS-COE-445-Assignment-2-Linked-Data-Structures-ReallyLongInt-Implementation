Download link :https://programming.engineering/product/cs-coe-445-assignment-2-linked-data-structures-reallylongint-implementation/


# CS-COE-445-Assignment-2-Linked-Data-Structures-ReallyLongInt-Implementation
CS/COE 445 Assignment 2 Linked Data Structures &amp; ReallyLongInt Implementation
Purpose: To give you experience implementing and using linked data structures.

Goal 1: To design and implement a class LinkedDS<T> that will act as a linked data structure for accessing Java Objects. Your LinkedDS<T> class will primarily implement two interfaces – PrimQ<T> and Reorder. The details of these interfaces are explained in the files PrimQ.java and Reorder.java. Read these files over very carefully before implementing your LinkedDS<T> class.

Goal 2: To utilize your LinkedDS<T> class to store and manipulate arbitrary length integers. We can think of an integer as a sequence of decimal digits. For example, the number 1234 could be stored as the digit ‘1’ followed by the digit ‘2’ followed by the digit ‘3’ followed by the digit ‘4’. We will store these digits in a linked chain. Clearly, to perform operations on a number that is stored in this fashion, we must access the digits one at a time in some systematic way. More specific details follow below.

DETAILS

Details 1: For the details on the functionality of your LinkedDS<T> class, carefully read over the files PrimQ.java, Reorder.java, and Assig2A.java provided on the CourseWeb folder where you find this assignment description. You must use these files as specified and cannot remove/alter any of the code that is already written in them. There are different ways of implementing the PrimQ<T> and Reorder interface methods, some of which are more efficient than others. Use only the best way of implementing these methods in this assignment. A lot of pencil and paper work is recommended before actually starting to write your code. Your LinkedDS<T> class header should be:

public class LinkedDS<T> implements PrimQ<T>, Reorder

The only instance variables allowed inside the LinkedDS<T> class are protected Node firstNode;

Assignment adapted from Dr. John Ramirez’s class.

protected int numberOfEntries;

Important Note: The primary data structure within LinkedDS<T> class must be a linked chain. You may not use any predefined Java collection class (e.g., ArrayList) for your LinkedDS<T> data.

Note that the following methods are added to the Reorder interface in this assignment as compared to Assignment 1.

public void leftShift(int num)

Shift the contents of the data structure num places to the left (assume the beginning is the leftmost node), removing the leftmost num nodes. For example, if a data structure has 8 nodes in it (numbered from 1 to 8), a leftShift of 3 would shift out nodes 1, 2 and 3 and the old node 4 would now be node 1. If num <= 0 leftShift should do nothing and if num >= the length of the data structure, the result should be an empty data structure.

public void rightShift(int num)

Same idea as leftShift above, but in the opposite direction. For example, if a data structure has 8 nodes in it (numbered from 1 to 8) a rightShift of 3 would shift out nodes 8, 7 and 6 and the old node 5 would now be the last node in the data structure. If num <= 0 rightShift should do nothing and if num >= the length of the data structure, the result should be an empty data structure.

Note that in the method implementation you may not create any new Node objects. The purpose of these methods is to rearrange the Nodes that already exist. To see how these should work, it is strongly recommended to draw one or more pictures.

You will also need to write the following constructors:

public LinkedDS()

public LinkedDS(LinkedDS<T> oldList)

The first constructor simply initializes the list to an empty state, and the second generates a new list that is a copy of the argument list (copying all of the nodes inside the old list).

Finally, you will need to override the following method:

public String toString();

This method will return a String that is the result of all of the data in the list being appended together, separated by spaces.

After you have finished your coding of LinkedDS<T>, the Assig2A.java file provided for you should compile and run correctly and should give output identical to the output shown in A2Out.txt.

Important Notes:

1) All of your LinkedDS methods must be implemented in an efficient way, utilizing the underlying linked chain. For example, a poor implementation of a left rotation could be done via repeated calls to X = removeItem() and addItem(X). However, doing this would require multiple

6
