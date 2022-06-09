# parallelcomputing
How I learned parallel computing in SUTD's May 2022 run of "50.049 Parallel Computing and Multicore Architectures"

As a creator, starting with full-stack software engineering, how will learning parallel computing help me?

Ok so I have convinced and inspired by the advantages of learning parallel computing, HMW make use of this code base to accelerate my learning in //comp? 
This repo is organised thematically through folders in the root proj directory.


## Motivation
### Hardware aspect
Multicore software processors are getting more and more widely accessible. 

### From the software perspectve...
The problem size
## In order to do //comp, need to understand hardware architectures - CPU and GPU
## Memory Organisation - UMA, NUMA (“from hardware’s POV)
## Put hardware and software - hardware-conscious computing 
    1. Parallel JOIN, Experimental Study(why damn lousy these days on common architectures) 
## When receiving a request to design a parallel program, how are we going to approach it?
    1. Methodology (so 
        1. Partition by data or tasks
        2. Then design how the tasks are going to communicate with each other
        3. Then design scheduling: whether to put several tasks together, in order to minimise communication between the tasks 
        4. Mapping: map a thread to a physical core
            1. NUMA vs UMA hardware architecture will affect this design step
            2. Using simple sorting algos/tiny computing problems to illustrate the concept of [ ] 
                1. “Bottom up/top-down”: each subtree can branch into one thread, then you can design how each thread is mapped to each core
## Week4: mem caches to evaluate correctness of problems
    1. locality: whether your program can explore spatial or temporal localties
## Reason behaviour of the program 
