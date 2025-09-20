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
TODO Question: What conclusions can you draw about the performance of LinkedList vs. ArrayList when omparing their running times for AddRemove vs. Access? Record those running times in README.txt!
-