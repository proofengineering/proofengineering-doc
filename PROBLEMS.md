Problems
========

This is a list of problem areas and issues that could conceivable be included in a proof engineering survey.

Proof Organization and Scalability
----------------------------------

- definition/specification languages (Gallina, Isabelle/Pure/HOL)
- library design
- constructs (type classes, modules, canonical structures, ...)
- encodings of structures (graphs as hypermaps, numbers as Church numerals, ...)
- proof object management (generation, size, ...)
- proofs by reflection vs. proofs by tactics
- proof languages (Isar, C-zar, ssreflect, ...)
- tactic languages (Ltac, Ltac2, Rtac, Mtac, ...)
- specialized proof procedures (SMT/SAT solvers, equational solving, sledgehammer, ...)
- domain-specific languages exportable to proof assistants
- strong specifications of functions using dependent types vs. companion lemmas
- proving vs. translation validation

Practical Proof Development and Evolution
-----------------------------------------

- library and module dependency management
- library packaging and versioning
- opaqueness and proof irrelevance in practice
- broken proofs in new proof assistant versions
- evolution-proof proofs
- proof repair
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

- metatheory, foundations and interpretations (sets, homotopy types, ...)
- admissible axioms (functional extensionality, classic, JMeq, ...)
- interface fidelity ("Pollack-inconsistency")
- extensions (plugins, patches, ...)
- de Bruijn principle
- core LOC and bugs
- independent checker implementations
- soundness of incremental checking (stale proofs)
- code extraction
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
