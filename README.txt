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