---
toc: true
comments: true
layout: post
title: Routing and Computing Team Teach
description: 
type: tangibles
courses: { compsci: {week: 1} }
---


## Popcorn Hack #1 (True or False)
image didn't show up


## Popcorn Hack #2 (MC)
image didn't show up

## Homework

[Flowcharts](https://www.canva.com/design/DAF3rLyXNeo/sWokp1z_imJBBkmDhvLm5g/edit?utm_content=DA[…]m_campaign=designshare&utm_medium=link2&utm_source=sharebutton)



## Sequential Execution

```python
import time

def sequential_task():
    for i in range(8):
        print(f"Sequential Task - Iteration {i + 1}")
        time.sleep(1)  # Simulating some work

if __name__ == "__main__":
    start_time = time.time()
    sequential_task()
    end_time = time.time()
    print(f"Sequential execution time: {end_time - start_time} seconds")
```

## Parallel Execution
```python
import time
import threading

def parallel_task(iteration):
    print(f"Parallel Task - Iteration {iteration + 1}")
    time.sleep(1)  # Simulating some work

def parallel_execution():
    threads = []
    for i in range(8):
        thread = threading.Thread(target=parallel_task, args=(i,))
        threads.append(thread)
        thread.start()
    for thread in threads:
        thread.join()

if __name__ == "__main__":
    start_time = time.time()
    parallel_execution()
    end_time = time.time()
    print(f"Parallel execution time: {end_time - start_time} seconds")

```