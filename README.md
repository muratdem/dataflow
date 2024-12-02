# Dataflow modeling
TLA+ model for Dataflow protocols

## Naiad clock
This TLA+ spec was available only as 13 pages of latexified pdf as part of the paper: "The Naiad Clock Protocol: Specification, Model Checking, and Correctness Proof"  https://www.microsoft.com/en-us/research/wp-content/uploads/2013/02/paper.pdf

I converted this to ASCII formatted version, and made some changes to spec to make it model checkable. There is a lot of definitions early on. The interesting part of the spec starts with variable definitions.


I also made changes for TLA-Web interactive exploration/simulation. In particular, I parametrized the next actions to enable us to see all enabled parametrized version of the action to pick for the next action in TLA-Web.

This link shows three points p3>p2, and p3>p1, with p1 and p2 initially having one record. The first action was chosen for Proc a to process the record at p1 and create a record for p3. The action created a local diff at `temp[a]` but that hasn't been shared with Proc b. `Temp` is basically the delta vector to update the current state. After all operations are performed and all updates are shared between processes, the state will quiesce at all processes. You can select any enabled action to advance the state, or go back to the previous state to choose another action.

https://will62794.github.io/tla-web/#!/home?specpath=https%3A%2F%2Fraw.githubusercontent.com%2Fmuratdem%2Fdataflow%2Frefs%2Fheads%2Fmain%2FNaiadClock.tla&constants%5BPoint%5D=%7Bp1%2Cp2%2Cp3%7D&constants%5BProc%5D=%7Ba%2Cb%7D&trace=731d71a6%2C231aa9af_06cd26d4&explodedConstantExpr=Point