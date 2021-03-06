Problems
========

This is a list of problem areas and issues that could conceivably be included in a proof engineering survey.

Proof Organization and Scalability
----------------------------------

- definition/specification languages (Gallina, Isabelle/Pure/HOL)
- library design
- constructs (type classes, modules, canonical structures, ...)
- encodings of structures (graphs as hypermaps, numbers as Church numerals, ...)
- proof object management (generation, size, ...)
- proof design principles (including domain-specific ones) [Talia]
- proofs by reflection vs. proofs by tactics
- proof languages (Isar, C-zar, ssreflect, ...)
- tactic languages (Ltac, Ltac2, Rtac, Mtac, ...)
- specialized proof procedures (SMT/SAT solvers, equational solving, sledgehammer, ...)
- domain-specific languages exportable to proof assistants
- strong specifications of functions using dependent types vs. companion lemmas
- proving vs. translation validation
- verification condition generation for domain-specific verification/refinement languages (Fiat, Why3, VeriFast, ...)

Practical Proof Development and Evolution
-----------------------------------------

- library and module dependency management
- library packaging and versioning
- opaqueness and proof irrelevance in practice
- broken proofs in new proof assistant versions
- evolution-proof proofs [Talia]
- proof repair [Talia]
- change impact analysis (incl. Ltac)
- regression proof selection
- regression proof prioritization
- continuous integration of verification projects
- parallel and distributed proving
- user interfaces
- testing of theorem statements (property-based testing)
- theory exploration (automatically stating and proving properties)
- interface responsiveness
- interface quality-of-life (reference autocompletion, dependency management, ...)
- interface support for refactorings
- human resource costs of formalization, verification, and proof maintenance
- proof reduction (removing redundant definitions and proofs)
- measuring completeness (and minimality) of properties w.r.t. defined inductive types and functions (e.g., via mutation analysis)

Reliability and Trusted Bases
-----------------------------

- metatheory, foundations, and interpretations (HOL, sets, homotopy types, ...)
- admissible axioms (functional extensionality, classic, JMeq, univalence, ...)
- interface fidelity ("Pollack-inconsistency")
- extensions (plugins, patches, ...)
- de Bruijn principle
- core size (LOC)
- core bugs in practice
- independent checker implementations (coqchk, ...)
- soundness of incremental checking (stale proofs, elided proof goals)
- code extraction from proof assistants to practical functional languages
- code compilation, self-hosted compilation
- metatheory in proof assistant itself and other proof assistants (Coq-in-Coq, NuPrl in Coq, ...)
- self-hosted proof checking (proof checking via Coq-in-Coq)
- validating formalizations against real-world implementations and hardware (x86-TSO, ...)

Social and Technological Impact
-------------------------------

- empirical validation of advantages
- proof assistants as general purpose programming environments
- proof assistant user training costs
- alleviating personal doubts about correctness
