# mini-exercise-5

## Part 3:
The java code creates 2 threads, each one takes calls a function that increments a general value 10,000 times. The threads are then started. 
The code then calls join which waits for both threads to finish. The threads run and each calls the function 10,000 times. Despite that, the value doesn't get to 20,000, the thread will read the value and then increment it. As a result, both threads might read the same value and increment it separately rendering one of the incrementations redundant. This way we get some value between 10,000 and 20,000 that is not constant and changes between runs.

## Part 4:
The updated java code includes the keyword "synchronized" when using the functions accessed in our code. This keyword allows a thread to create an intrinsic lock on a function when accessing it. This way, only one thread accesses the data at a time, allowing all of the increments to act and allowing the number to grow all the way to 20,000 (using all of the increment calls).
