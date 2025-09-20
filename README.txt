
TestIterator:
TODO Question: Also try with a LinkedList - does it make any difference?
- Functionally no difference, both tests pass.
TODO Question: What happens if you use list.remove(Integer.valueOf(77))?
- It throws ConcurrentModificationException if called while iterating, because the list is modified outside the iterator.

TestList:
TODO Question: What happens if you use list.remove(Integer.valueOf(77))?
- Removes first occurence of 77.
 TODO Question: What does this method do? list.remove(5); //
- removes element at index 5.
TODO Question: What does this one do? list.remove(Integer.valueOf(5)); //
- Removes first occurence of 5, like in case of 77 previously.

TestPerformance:
TODO Question: What conclusions can you draw about the performance of LinkedList vs. ArrayList when comparing their running times for AddRemove vs. Access? Record those running times in README.txt!
- As SIZE increases, Array stays very efficient throughout for access, but very innefficient for addRemove.
- LList on the other hand, stays very efficient for add/remove, but very slow for access.

	SIZE 10
								  #1   #2   #3   #4   #5   #6 	... (as many tests as you ran)
        testArrayListAddRemove:  277.55 284.01 287.87 281.53 268.78 289.70  ... (fill these in in ms)
        testLinkedListAddRemove: 26.76 24.94 23.89 25.11 22.63
		testArrayListAccess:     8.81 8.87 9.86 8.70 9.82 8.19
        testLinkedListAccess:    12.00 10.59 11.55 11.92 10.67 14.66

	SIZE 100
								  #1   #2   #3   #4   #5   #6 	... (as many tests as you ran)
        testArrayListAddRemove:  296.43 300.92 312.28 295.13 296.11 295.16  ... (fill these in in ms)
        testLinkedListAddRemove: 23.57 29.74 22.64 22.99 24.42 27.86
		testArrayListAccess:     9.57 9.32 8.83 10.24 9.42 9.16
        testLinkedListAccess:    20.87 23.98 22.42 22.54 24.44 23.76

	SIZE 1000
								  #1   #2   #3   #4   #5   #6 	... (as many tests as you ran)
        testArrayListAddRemove:  22.24 27.23 23.95 38.72 25.72 26.45  ... (fill these in in ms)
        testLinkedListAddRemove: 401.46 373.95 404.54 395.15 461.10 373.02
		testArrayListAccess:     9.21 10.62 9.16 9.19 9.63 9.18
        testLinkedListAccess:    270.64 278.38 275.49 278.21 283.57 272.35

	SIZE 10000
								  #1   #2   #3   #4   #5   #6 	... (as many tests as you ran)
        testArrayListAddRemove:  1443.1 1425.4 1871.5 1831.8 1844.7 1842.7  ... (fill these in in ms)
        testLinkedListAddRemove: 24.73 24.70 27.94 26.11 28.45 24.80
		testArrayListAccess:     11.68 9.00 12.68 10.29 8.18 13.36
        testLinkedListAccess:    5005.3 6203.7 6067.3 5844.9 6184.2 6498.9


     Also I ran the whole Test Performances for adjusted REPS, and the higher REPS resulted in longer run times.

     BUILD SUCCESSFUL in 1s
     2 actionable tasks: 1 executed, 1 up-to-date
     10:14:26 PM: Execution finished ':test --tests "cs271.lab.list.TestPerformance.testLinkedListAddRemove"'.

     BUILD SUCCESSFUL in 7s
     2 actionable tasks: 1 executed, 1 up-to-date
     10:13:19 PM: Execution finished ':test --tests "cs271.lab.list.TestPerformance.testArrayListAddRemove"'.

