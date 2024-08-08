+++
title = "Fetch Unit"
date = "2024-08-08"
description = "Fetch Unit in CPU"
+++

In a CPU, the fetch unit is a critical component responsible for retrieving instructions from memory. 
It uses the program counter (PC) to get the next instruction, updates the PC, and may use an instruction cache to speed up retrieval.
It may also involve branch prediction and prefetching to enhance performance and keep the instruction pipeline full.
We will look into designing a Fetch Unit with Branch Prediction. This would require us to add flush capability to the stage.

## Flush
The Pipeline needs to be flushed i.e. needs to start from scratch when we take the wrong branch.
In this architecture only the execution unit decides if flush is required

## Branch Prediction
FU predicts the next instuction that needs to be fetched. Either PC+4 or Address that is Jumped 
This is decided based on logic to minimize wrong prediction
1. Take unconditional branch
2. Take backward branch
3. Do not Take forward branch
Branch Prediction also can locally flush the FU when branch is taken
