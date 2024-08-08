+++
title = "Introduction to CPU"
date = "2024-08-01"
description = "Introduction to CPU and RISC pipeline"
+++

CPU are integral part of all computers, How do they actually work?

Modern CPUs are complex devices made from simple rules. They essentailly only do a few things
* fetch an instruction
* decode the instrcution to perform a simple operation
* execute the operation (ADD, MOVE, etc)
* memory is accessed if required
* write back the result of the operation to memory

The above discribes the a CPU pipeline, specifically a RISC CPU Pipeline. Pipelining helps the CPU to run faster, it introduces concurrency into the picture. Instruction can be decoded at the same time the next instruction can be fetched.

Modern CPU architectures follow the same ideas with additional complexity to achieve higher speed or power efficiency. This includes instruction compression, out of order execution, complex memeory hierarchy and multi-cores. In future posts we'll look into designing a simple RISC-V CPU.
