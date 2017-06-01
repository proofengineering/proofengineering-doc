---
title: 'QED in the Large: A Survey of Engineering of Machine-Checked Proofs'
author: Authors
...

# Introduction

Development of formal, machine-checked proofs of general mathematical theorems and correctness of programs can increase their actual and perceived reliability and facilitate better understanding of underlying assumptions @Yang2011. Frameworks and tools supporting such development have been available for over 40 years @Bjoerner2014, but have only recently seen wider practical use in the research community. 

In fact, projects based on construction and certification of machine-checked proofs are now reaching an unprecedented scale, comparable to large software engineering projects. For example, the proof of the Feit-Thompson odd order theorem in the Coq proof assistant was a six-year effort of a team of 15 people, resulting in 170,000 lines of specification and proofs @Gonthier2013. Similarly, the proof of correctness for an operating system kernel in the Isabelle/HOL proof assistant took around 20 person years to develop, and as of 2014 consisted of 480,000 lines of specifications and proofs @Klein2014micro.

Scale leads to new problems and increasing need for tool support in proof development and maintenance. For example, properties to prove may have to be reformulated to facilitate library reuse @hales-kepler, and mathematical structures encoded in specific ways to allow proofs about them to be automated @Gonthier2008. Proof development environments should allow users to efficiently write, check, and share proofs; repositories of formal mathematics should allow easy search and seamless integration of results into local projects. Evolving projects face the possibility of previous proofs breaking due to seemingly unrelated changes, requiring support for quick error detection and repair.

We believe that significant research effort is needed to properly address such _proof engineering_ issues that large scale projects are subject to. In particular, considerable inspiration can be drawn from previous work in the software engineering community on large-scale development practices and tools @Klein2014. However, despite of the close conceptual ties between software and proof construction, research from software engineering require careful adaptation to transfer to the world of formal proofs, where concerns about underlying logical foundations and frameworks are the norm.

Despite its increasing importance, proof engineering is seldom considered in its own right; related theories, techniques, and tools span a many fields and venues. This survey of the literature is an attempt at a more unified and holistic understanding of proof engineering, in particular in the context of proof assistants with powerful theoretical underpinnings such as dependent types and higher-order logic.

# Overview

We organize proof engineering related research under four headings: (a) proof organization and scalability, (b) practical proof development and and evolution, (c) reliability and trusted bases, (d) technological and social impact.

At a glance, (a) concerns specific languages and methods to obtain and organize proofs, (b) concerns developer practices and tools, (c) explains foundational issues such as choice of axioms, and (d) covers applications and consequences of proof engineering for mathematics and computer science.

\bibliography{references}
