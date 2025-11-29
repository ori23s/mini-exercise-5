# mini-exercise-5

## Part 3:
The java code creates 2 threads, each one takes calls a function that increments a general value 10,000 times. The threads are then started. 
The code then calls join which waits for both threads to finish. The threads run and each calls the function 10,000 times. Despite that, the value doesn't get to 20,000, the thread will read the value and then increment it. As a result, both threads might read the same value and increment it separately rendering one of the incrementations redundant. This way we get some value between 10,000 and 20,000 that is not constant and changes between runs.

## Part 4:
The updated java code includes the keyword "synchronized" when using the functions accessed in our code. This keyword allows a thread to create an intrinsic lock on a function when accessing it. This way, only one thread accesses the data at a time, allowing all of the increments to act and allowing the number to grow all the way to 20,000 (using all of the increment calls). 
## Part 5:
Here, the result is identical to part 4 as the part of the code that has the double access to the incrementation is still synchronized. The synchronized keyword on the block gives it an intrinsic lock and this way the same code is still synchronized. We get the same result and the code still increments up to 20,000.
## Part 6:
This code creates 10 threads and runs just like in part 3, each one increments the variable 10 million times (without synchronization), the code also tracks the amount of time the code takes to run, my initial result was 22 and I ran it a few more times (not all runs will take the same amount of time) and all of them were in that general vicinity. The program takes 10 threads, each increments 10 million times (we don't get all the way to 100 million since it isn't synchronized, our program takes around 22 milliseconds.
