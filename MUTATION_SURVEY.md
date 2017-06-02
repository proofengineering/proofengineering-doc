Mutation Testing in Functional Languages
----------------------------------------

Le et al. (2014; http://doi.acm.org/10.1145/2610384.2628052) implemented a tool, MuCheck, for mutation testing of Haskell programs. The built-in mutation operators take three forms:

1. reordering of pattern matching clauses in functions
2. reordering and replacement in list expressions
3. type-aware function replacement (e.g., replace functions of type A -> A with the identity function)

Further mutation operators can be defined by the framework user. In the implementation, operators are applied nondeterministically at the level of abstract syntax trees. The tool is demonstrated in a case study involving sorting of lists via the Quicksort algorithm and random tests using the QuickCheck framework.

Duregård (2016; http://publications.lib.chalmers.se/records/fulltext/240807/240807.pdf) proposes an approach to black-box mutation testing of functional code, where a user has no knowledge of or access to the system under test but still wants to know the strength of some property expressed in a property-testing framework. Each generated (random) test case is run both on the original function and a randomly selected mutant of the function. The mutation score is defined as the probability that a random mutant survives a random test case, and the user obtains an estimate of this probability by sampling. The function under test must be an instance of a specific type class that allows it to be mutated (without modifying it in-place). The implementation is carried out on top of regular QuickCheck in Haskell.

Braquehais and Runciman (2016; http://doi.acm.org/10.1145/2976002.2976003) present a Haskell framework, FitSpec, that uses mutation testing to measure adequacy of sets of properties specified in property-testing frameworks such as QuickCheck and SmallCheck. The stated goal is to assist in determining both the completeness and minimality of a proposed property set. If either is lacking, output from FitSpec can help refining the property set. FitSpec takes a black-box view of mutations, and uses enumeration to produce mutants.

Taylor and Derrick (2015; http://dx.doi.org/10.1007/978-3-319-25945-1_11) present a more traditional mutation testing framework for Erlang, mu2, which supports user-specified mutation operators. The framework is evaluated on an industrial codebase.

Coverage in Functional Languages
--------------------------------

Gill and Runciman (2007; http://doi.acm.org/10.1145/1291201.1291203) proposed a now widely adopted measure of coverage for Haskell programs, primarily based on coverage of (sub-)expressions inside functions. Cheng et al. (2016; http://dx.doi.org/10.1109/ICST.2016.8) evaluate effectiveness of coverage for Haskell programs, and conclude that findings from imperative programs hold in general, but that results vary for specific criteria; mutation testing via MuCheck is used in the evaluation.

Mutation Analysis for Verification
----------------------------------

Groce et al. (2015; http://dx.doi.org/10.1109/ASE.2015.40) use mutation-based analysis approach to improving verification based on model checking. The goal of mutating a formal model is to facilitate better understanding of whether successful verification actually implies a desired property. In addition to mutating the model, verification efforts must also be guided to cover mutated code. According to the authors, no previous work presented passing executions of a source code mutant as a guide to understanding specification weakness.

Property-Based Testing in Proof Assistants
------------------------------------------

In property-based testing, programmers specify (efficiently computable) properties about functions, along with generators for input data to those functions. A property testing framework then samples test cases randomly, runs them, and reports the results. Property-based testing was first popularized for Haskell (QuickCheck, SmallCheck) and Erlang (QuickCheck).

Over the years, many verification environments (including proof assistants such as Isabelle/HOL), have been equipped with integrated support for property-based testing, primarily for use in counter-example generation. Paraskevopoulou et al. (2015; http://dx.doi.org/10.1007/978-3-319-22102-1_22) recently implemented QuickCheck inside Coq in a framework dubbed QuickChick. Besides specifying properties to check and data generators, QuickChick allows connecting executable properties to their purely logical counterparts inside Coq to ensure the expected property is tested. For performance reasons, the randomized tests are run outside of Coq in an OCaml environment. 
