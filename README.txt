I ran the SIZE and REPS in different numbers and found that when I tuned REPS to twice the amount, it ran for 3 seconds instead of 2. When I tuned it to 20 million and tuned SIZE to 200, it took 7 seconds.

So:

1) SIZE 100 REPS 200,000 = 2 seconds
2) SIZE 100 REPS 400,000 = 3 seconds
3) SIZE 200 REPS 20 000 000 = 7 seconds

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
-No performance difference at default scales, however I noticed a big difference in  LL and Array AddRemove functions when scaling out the REPS to 20 million again. Here:
6 second difference

BUILD SUCCESSFUL in 1s
2 actionable tasks: 1 executed, 1 up-to-date
10:14:26 PM: Execution finished ':test --tests "cs271.lab.list.TestPerformance.testLinkedListAddRemove"'.

BUILD SUCCESSFUL in 7s
2 actionable tasks: 1 executed, 1 up-to-date
10:13:19 PM: Execution finished ':test --tests "cs271.lab.list.TestPerformance.testArrayListAddRemove"'.

No difference noted when scaling out the size in any function.

//

State how many times the tests were executed for each SIZE (10, 100, 1000 and 10000)
	to get the running time in milliseconds and how the test running times were recorded.

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
		testArrayListAccess:     val1 val2 val3 val4 val5 val6
        testLinkedListAccess:    val1 val2 val3 val4 val5 val6

	SIZE 1000
								  #1   #2   #3   #4   #5   #6 	... (as many tests as you ran)
        testArrayListAddRemove:  val1 val2 val3 val4 val5 val6  ... (fill these in in ms)
        testLinkedListAddRemove: val1 val2 val3 val4 val5 val6
		testArrayListAccess:     val1 val2 val3 val4 val5 val6
        testLinkedListAccess:    val1 val2 val3 val4 val5 val6

	SIZE 10000
								  #1   #2   #3   #4   #5   #6 	... (as many tests as you ran)
        testArrayListAddRemove:  val1 val2 val3 val4 val5 val6  ... (fill these in in ms)
        testLinkedListAddRemove: val1 val2 val3 val4 val5 val6
		testArrayListAccess:     val1 val2 val3 val4 val5 val6
        testLinkedListAccess:    val1 val2 val3 val4 val5 val6