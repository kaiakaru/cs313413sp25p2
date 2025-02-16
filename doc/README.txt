COMP 313/413 Project 2 Report Template

TestList.java and TestIterator.java

	TODO also try with a LinkedList - does it make any difference?

		In TestList and TestIterator the program compiles and builds successfully whether you use a LinkedList or an
		ArrayList. After testing each multiple times, the time complexity is similar in each. LinkedLists
		should be quicker for removing and adding items while ArrayLists are quicker for accessing items.

TestList.java

	testRemoveObject()

		list.remove(5); // what does this method do?

			This method removes the element in the 5th index.

		list.remove(Integer.valueOf(5)); // what does this one do?

			This method removes the element(s) with the integer value 5.

TestIterator.java

	testRemove()

		i.remove(); // what happens if you use list.remove(77)?

			The test fails because list.remove(77) refers to the index, but the size of the list is 7,
			so the program threw an exception. The iterator doesn't expect external changes of the list structure.

TestPerformance.java

	State how many times the tests were executed for each SIZE (10, 100, 1000 and 10000)
	to get the running time in milliseconds and how the test running times were recorded.
	These are examples of SIZEs you might choose, you can choose others if you wish.

	SIZE 10
								  #1   #2   #3   #4 	... (as many tests as you ran)
        testArrayListAddRemove:  18.7 17.1 16.9 17.6    ... (fill these in in ms)
        testLinkedListAddRemove: 15.9 14.3 14.6 14.6
		testArrayListAccess:     9.11 9.56 10.1 11.4
        testLinkedListAccess:    6.58 6.37 6.46 6.23

	SIZE 100
								  #1   #2   #3   #4    ... (as many tests as you ran)
        testArrayListAddRemove:  5.75 6.08 5.69 6.59   ... (fill these in in ms)
        testLinkedListAddRemove: 5.35 4.89 4.89 5.95
		testArrayListAccess:     3.72 3.63 3.87 3.82
        testLinkedListAccess:    5.12 5.16 5.14 5.41

	SIZE 1000
								  #1   #2   #3   #4  	... (as many tests as you ran)
        testArrayListAddRemove:  2.36 3.61 2.36 2.87    ... (fill these in in ms)
        testLinkedListAddRemove: 1.22 1.99 1.31 4.36
		testArrayListAccess:     .503 .364 .357 .304
        testLinkedListAccess:    5.27 7.56 5.44 5.81

	SIZE 10000
								  #1   #2   #3   #4    ... (as many tests as you ran)
        testArrayListAddRemove:  3.32 3.42 3.67 3.19   ... (fill these in in ms)
        testLinkedListAddRemove: .388 .439 .645 .416
		testArrayListAccess:     .038 .039 .041 .048
        testLinkedListAccess:    1.09 1.11 1.14 1.15

	listAccess - which type of List is better to use, and why?

		An ArrayList is better to use because it is backed by an array so there's easy access by index.
		A LinkedList would have to traverse through the other elements to access the desired one.

	listAddRemove - which type of List is better to use, and why?

		LinkedLists are better for adding and removing operations because the pointers are just being updated, meanwhile
		an ArrayList would need to shift all the other elements when one is being removed or inserted.
