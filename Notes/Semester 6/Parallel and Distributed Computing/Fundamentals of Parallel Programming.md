## What is Parallel Programming

- Use of multiple processors or machines working together on a common task
- Each processor/machine works on its section of the problem
- Processors may exchange information
## Why Parallel Programming

- increases performance substantially
- but at the cost of complexity
- utilize more than 1 cores by dividing the task into multiple pieces
## How parallel computation works

For parallel computation to work we need multiple processors connected to memory that is either pooled or connected via high speed networks.

**Types of Parallel Computation**

Shared Memory Model:
All processors share the same memory.

![[Screenshot from 2024-01-31 01-05-38.png]]

Distributed Memory Model:
- every processor has it's own memory
- information shared using a network

![[Screenshot from 2024-01-31 01-08-08.png]]

Distributed/Shared Model
- hybrid system
- processors have there own memory
- all processors share a common memory as well

![[Screenshot from 2024-01-31 01-05-59.png]]

## Two main Aspects of Parallel Computing

1. Technology Push
2. Applications Pull

**Technology Push**

From the mid 1980 to the 2004's computer got fast
- more transistors
- higher clock speed

Moore's Law limit reached
Thermal Wall reached

Companies started making multi-core Processors

**Application Pull**

Traditionally software was written in serial computaion


[Reference](https://curc.readthedocs.io/en/latest/programming/parallel-programming-fundamentals.html)