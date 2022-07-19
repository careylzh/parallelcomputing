# parallelcomputing
How I learned parallel computing in SUTD's May 2022 run of "50.049 Parallel Computing and Multicore Architectures"

As a creator, starting with full-stack software engineering, how will learning parallel computing help me?

Ok so I have convinced and inspired by the advantages of learning parallel computing, HMW make use of this code base to accelerate my learning in //comp? 
This repo is organised thematically through folders in the root proj directory.

## How this Course is Organised
The first 4 week
### 3 main blocks:
- week 1234: gaining interest for this course through understanding the powers of //comp, toy problems and basic technical concepts like cache coherence 
    - As engineers, why learn //comp? (brief intro of where //comp, this helps us build sufficient knowledge about what //comp is about so we can keep up with subsequent weeks)
    - Foster's Design Methodology: the 4 steps used to approach a problem to parallelise it (could be applied on existing problems designed of a different computing paradigm, or to design new solutions for a new problem statement) 
    - Toy problems: `FactorPrime`
    - Small-scale parallelization of real-life operations (eg. Canonical Hash Join, a real database query which queries 2 tables and combines the sub results from each table into 1 output) 
    - Building blocks of //comp: the fundamental algos used to design bigger pieces of knowledge, understand rsp. complexity improvements:
        - parallelised bubble sort
        (**TODO: these algos will be used as the fundamental building blocks of subsequent. but which week content?**) 
    - Cache coherence 
- week 568:
Week 568: how to implement correct parallel programs, check for correctness of 
Week 91011: KPI measurement
Week 12: Adv topics 
13: Review     

## Motivation

### Hardware aspect
Multicore software processors are getting more and more widely accessible. 

### From the software perspectve...
The problem size is rapidly increasing, and the performance demand is more and more strict. The idea is to write programs that capitalise on the resources of your entire system to increase performance(more in week 11 on how to define KPIs for measure //comp performance)

## Parallel Architectures

In order to do //comp, need to understand hardware architectures - CPU and GPU
### Processor Architectures
- Memory Organisation - UMA, NUMA (“from hardware’s POV)
### Harmonizing hardware software = hardware-conscious computing 
    1. Example of problems in this section: Parallel JOIN, Experimental Study(why damn lousy these days on common architectures) 

## Methodologies
### When receiving a request to design a parallel program, how are we going to approach it?
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
