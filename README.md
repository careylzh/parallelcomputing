# parallelcomputing
How I learned parallel computing in SUTD's May 2022 run of "50.049 Parallel Computing and Multicore Architectures"

**As a creator who is starting his/her career in full-stack software engineering, how will learning parallel computing help me?**
"*If I take a stone's throw measurement of who knows parallel computing in my workplace, very few people know it. I think the point of learning things as an undergraduate is s.t. when we need it we will be like 'oh I think I have come across this before in [mod]. '*" ~ Anecdote from senior who graduated at 3-4 years ago  

Now that I am inspired by the advantages of learning parallel computing, HMW make use of this code base to accelerate my learning in //comp? 
This repo is organised thematically through folders in the root proj directory (**TODO:** decide whether to put code examples here or just pseudo-code, since not every1 who wants to learn //comp is a Java or C++ developer. But hey - Java/C++ libraries streamline the implementation of //comp for developers)

## How this Course is Organised
The first 4 weeks are important because they build //comp intuitions - keywords, ways of visualising //comp patterns, high-lvl overview of problems(addressed by //comp). Listen in class to see how prof draws stuff when visualising things like stream processing solutions.

The next 4 weeks focus on implementing parallel programs and testing for their correctness. If you think you're alr decent at this, go beyond correctness and ensure that your solution is more efficient (than the previous one). 

The last few weeks focuses systematising all knowledge learnt thus far into design patterns, and parallel program performance analysis - *how do we compose a fair set of engineering KPIs to measure the performance of parallel programs?*
### 3 main blocks:
- **week 1234**: gaining interest for this course through understanding the powers of //comp, toy problems and basic technical concepts like cache coherence 
    - As engineers, why learn //comp? (brief intro of where //comp, this helps us build sufficient knowledge about what //comp is about so we can keep up with subsequent weeks)
    - Foster's Design Methodology: the 4 steps used to approach a problem to parallelise it (could be applied on existing problems designed of a different computing paradigm, or to design new solutions for a new problem statement) 
    - Toy problems: `FactorPrime`
    - Small-scale parallelization of real-life operations (eg. Canonical Hash Join, a real database query which queries 2 tables and combines the sub results from each table into 1 output) 
    - Building blocks of //comp: the fundamental algos used to design bigger pieces of knowledge, understand rsp. complexity improvements:
        - parallelised bubble sort
        (**TODO: these algos will be used as the fundamental building blocks of subsequent. but which week content?**) 
    - Cache coherence 
- **week 5689**: challenges in implementing correct //comp programs and techniques
  - synchronization
  - liveness hazards
  - thread safety + its design principles
    -(** TODO: refine - what I rmb: **)
      - change of data structures used: `LinkedList`(not thread safe) --> `LinkedBlockingQueue`
- **week 101112**: //comp Design Patterns, KPI measurement, "Adv topics"**(week 12, TODO)**
  - week 10 design patterns: 8 of them
  (**TODO: linear search for possible missing patterns in notes**)
    - Fork-join
    - Parbegin-parend 
    - SIMD
    - **SPMD**
    - **Pipelining**
    - **Master-Worker**
    - **Client-Server**
    - **Producer-Consumer**
## Motivation

### Hardware aspect
Multicore software processors are getting more and more widely accessible. 

### From the software perspectve...
The problem size is rapidly increasing, and the performance demand is more and more strict. The idea is to write programs that capitalise on the resources of your entire system to increase performance(more in week 11 on how to define KPIs for measure //comp performance)

## Parallel Architectures

In order to do //comp, need to understand hardware architectures - CPU and GPU
### Processor Architectures
- Memory Organisation - UMA, NUMA (???from hardware???s POV)
### Harmonizing hardware software = hardware-conscious computing 
    1. Example of problems in this section: Parallel JOIN, Experimental Study(why damn lousy these days on common architectures) 

## When receiving a request to design a parallel program, how are we going to approach it?
This is the highest-lvl problem solving approach of this course. We are going to use this thinking process to approach every parallel computing problem.
### Foster's Design Methodology
1. Partition by data or tasks
2. Communicate: Secondly, design how the tasks are going to communicate with each other
3. Agglomerate: collect or form into a mass or group. In this case we are handling design scheduling: whether to put several tasks together, in order to minimise communication between the tasks
4. Map: design a mapping system to map rsp. threads to rsp. physical computing cores. Doing so will help you explore and better understand your data/task requirements
   1. need to identify if hardware architecture is NUMA vs UMA, as (**TODO**)
   2. Using simple sorting algos/tiny computing problems learnt in prev week to illustrate the concept of [ ] 
      1. ???Bottom up/top-down???: each subtree can branch into one thread, then you can design how each thread is mapped to each core
## Week4: mem caches to evaluate correctness of problems
    1. locality: whether your program can explore spatial or temporal localties
### Intuitions 
- Try to reason behaviour of the each solution provided 
