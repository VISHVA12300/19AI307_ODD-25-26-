# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Use a **synchronized block** (NOT a synchronized method) to safely increment a **shared counter** using multiple threads.

Each thread performs a number of increments on the same counter, and the synchronized block must prevent race conditions.

### Input:
- `n` → number of threads  
- `increments` → how many times each thread increments the counter  

### Output:
```
Final count: <value>
```

---

## AIM:
To write a Java program that demonstrates thread synchronization using a **synchronized block** to safely update shared data.

---

## ALGORITHM :
1. Start the program.  
2. Read the number of threads and number of increments per thread.  
3. Create a shared `Counter` object holding the integer `count`.  
4. Create a shared `lock` object for synchronization.  
5. Create `n` threads; each thread runs a loop of `increments` times.  
6. Inside each loop iteration, use a **synchronized(lock)** block to increment the shared counter.  
7. Start all threads.  
8. Use `join()` to wait for all threads to finish.  
9. Print the final value of the counter.  
10. End the program.

---

## PROGRAM:
```
/*
Program to safely increment a shared counter using synchronized block
Developed by: VISHVA V
Register Number: 212222040182
*/
```

## Sourcecode.java:
```java
import java.util.*;

class Counter {
    int count = 0;
}

public class SyncBlockExample {
    public static void main(String[] args) throws InterruptedException {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt(); // number of threads
        int increments = sc.nextInt(); // increments per thread

        Counter counter = new Counter();

        Thread[] threads = new Thread[n];
        Object lock = new Object(); // shared lock object

        for (int i = 0; i < n; i++) {
            threads[i] = new Thread(() -> {
                for (int j = 0; j < increments; j++) {
                    synchronized (lock) {
                        counter.count++;
                    }
                }
            });
            threads[i].start();
        }

        for (Thread t : threads) t.join();

        System.out.println("Final count: " + counter.count);
        sc.close();
    }
}
```

---

## OUTPUT:
<img width="545" height="309" alt="image" src="https://github.com/user-attachments/assets/a77fb2b3-d355-49bf-93af-e8c3b7861555" />


---

## RESULT:
Thus, the program successfully demonstrates the use of a **synchronized block** to ensure safe access to shared data across multiple threads.
