# Dataflow modeling
TLA+ model for Dataflow protocols

## Naiad clock
This TLA+ spec was available only as 13 pages of latexified pdf as part of the paper: "The Naiad Clock Protocol: Specification, Model Checking, and Correctness Proof"  https://www.microsoft.com/en-us/research/wp-content/uploads/2013/02/paper.pdf

I converted this to ASCII formatted version, and made some changes to spec to make it model checkable. 

I also made changes for TLA-Web interactive exploration/simulation. In particulare, I  parametrized rhw next actions to enable us to see all enabled parametrized version of the action to pick for the next action in TLA-Web.

There is a lot of definitions early on. The interesting part of the spec starts with variable definitions.
