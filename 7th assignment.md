# 7th Assignment
//Maryam Modanloo • 400222094//
### Pi Calculator:
In this code, i define a PiCalculator class that has a calculate method that takes an integer floatingPoint as input and returns a string representation of pi with the given number of digits after the decimal point. The calculation is done using a multi-threaded approach where we split the work into multiple threads and combine the results at the end.

I define a PiThread class that extends Thread and does the actual calculation of pi for a given range of values. Each thread calculates a partial sum of pi using the Leibniz formula for pi. I use the BigDecimal class to perform arbitrary-precision arithmetic and avoid rounding errors.

In the calculate method, i create THREAD_COUNT number of threads and distribute the work among them. I then wait for all threads to finish and add up their partial sums to get the final value of pi. Finally, i round off the result to floatingPoint number of digits after the decimal point using BigDecimal's setScale method.
### Priority:
In this code, i used the Thread.setPriority() method that set the priority in range of 1-10 for every thread.
Priority 1: Thread.MIN_PRIORITY
Priority 5: Thread.NORM_PRIORITY
Priority 10: Thread.MAX_PRIORITY
I used this method in every thread type’s run() method and in Runner’s run() method in defined loops.
I used the CountDownLatch class too but i didn’t achieve any successful result :) . At least i tried!
### Semaphore: 
In this code , i used Semaphore to limit the threads to access the resource.we use semaphore in the thread synchronization.
With “Semaphore semaphore = new Semaphore(available permissions)”
In thread’s run() method we should call Semaphore.acquire.The method acquire the permits from the semaphore, blocking until one is available, or the thread is interrupted. It reduces the number of available permits by 1.
At the end , we call release().  This method releases a permit and returns it to the semaphore. It increments the number of available permits by 1.


