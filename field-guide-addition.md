## Historical Note: Framework Fabrication Has a 44-Year-Old Precedent

The diagnostic vocabulary in this guide — particularly Framework Fabrication Syndrome — is not just an observed AI failure pattern. It is the *absence* of an engineering property that constraint-oriented systems have possessed since 1981.

In Alan Borning’s ThingLab (1981), a constraint-oriented simulation laboratory built at Xerox PARC, the system had an explicit architectural property: when constraints were genuinely unsatisfiable, it reported failure. When asked to find real-number solutions to equations with only complex roots, ThingLab put up an error message. It did not fabricate a plausible-looking answer.

This is not a minor implementation detail. It is a fundamental design choice: **a system that cannot satisfy its constraints must say so.**

Every major AI language model lacks this property. When an LLM cannot satisfy the implicit constraint “give a correct, grounded answer,” it does not report failure. It generates a plausible-looking fabrication — a nonexistent citation, an invented methodology, a confident falsehood. The user experiences this as helpful behavior. It is the opposite.

Framework Fabrication Syndrome is therefore not a novel AI pathology. It is the predictable consequence of deploying systems that lack an honest failure mode — a property the constraint programming community implemented and validated before most current AI researchers were born.

The naming matters because it reframes the problem. FFS is not a bug to be patched with better training data. It is a missing architectural layer — the same layer Borning built into ThingLab in 1981, and the same layer the Frozen Kernel proposes for modern AI systems.

**Reference:** Borning, A. “The Programming Language Aspects of ThingLab, a Constraint-Oriented Simulation Laboratory.” *ACM Transactions on Programming Languages and Systems*, Vol. 3, No. 4, October 1981, pp. 353–387. https://doi.org/10.1145/357146.357147
