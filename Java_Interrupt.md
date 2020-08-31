
Understanding Thread Interruption in Java

https://praveer09.github.io/technology/2015/12/06/understanding-thread-interruption-in-java/#:~:text=In%20Java%2C%20one%20thread%20cannot,as%20true%20on%20the%20instance.

Summary

The answers to the two questions that I had set out to answer are:

How to request a task, running on a separate thread, to finish early? 
- Use interruption.
If using Thread directly in your code, you may call interrupt() on the instance of thread.

If using Executor framework, you may cancel each task by calling cancel() on Future

If using Executor framework, you may shutdown the ExecutorService by calling the shutdownNow() method.

How to make a task responsive to such a finish request? 

Handle interruption request, which in most of the cases is done by handling InterruptedException. Also preserve the interruption status by calling Thread.currentThread().interrupt().
