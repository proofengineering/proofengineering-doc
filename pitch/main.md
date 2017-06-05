---
title: 'QED at Large: A Survey of Engineering of Machine-Checked Proofs'
author: Authors
...

# Introduction

Development of formal, machine-checked proofs of correctness of programs and mathematical theorems can increase their actual and perceived reliability and facilitate better understanding of underlying assumptions (@Yang2011). Frameworks and tools supporting such development have been available for over 40 years (@Bjoerner2014), but have only recently seen wider practical use in academia and industry.

In fact, projects based on construction of machine-checked proofs are now reaching an unprecedented scale, comparable to that of large software engineering projects. For example, the correctness proofs for an operating system kernel took around 20 person years to develop in the Isabelle/HOL proof assistant, and as of 2014 consisted of 480,000 lines of specifications and proof scripts (@Klein2014micro). Along similar lines, the proof of the Feit-Thompson odd order theorem in the Coq proof assistant was a six-year effort of a team of 15 people, resulting in 170,000 lines of specifications and proof scripts (@Gonthier2013).

Scaling up leads to new problems and additional demand for tool support in proof development and maintenance. For example, properties to prove may have to be reformulated to facilitate library reuse (@hales-kepler), and mathematical structures encoded in specific ways to allow proofs about them to be automated (@Gonthier2008). Proof development environments need to allow users to efficiently write, check, and share proofs; repositories of formal mathematics need to allow easy search and seamless integration of results into local projects. Evolving projects face the possibility of previous proofs breaking due to seemingly unrelated changes, requiring support for quick error detection and repair.

We believe that significant, sustained effort by the research community is needed to properly address such _proof engineering_ issues that large projects are subject to. In particular, considerable inspiration can be drawn from previous work in the software engineering community on large-scale development practices and tools (@Klein2014). However, even with close conceptual ties between software and proof construction, research in software engineering requires careful translation to the world of formal proofs. For example, regression testing research can become applicable by considering lemmas and their proofs in place of tests, i.e., for the purpose of _regression proving_; yet, the standard programming language metric used to prioritize regression tests---statement coverage---has no straightforward analogue for lemmas with complex conditions and quantification.

Despite its increasing importance, proof engineering is seldom considered in its own right; related theories, techniques, and tools span many fields and venues. This survey of the literature is an attempt at a more unified and holistic understanding of proof engineering, in particular in the context of proof assistants with powerful theoretical underpinnings based on, e.g., dependent types and higher-order logic.

# Overview

We survey proof engineering-related research under four headings: (a) proof organization and scalability, (b) practical proof development and evolution, (c) reliability and trusted bases, (d) technological and social impact.

At a glance, (a) concerns specific languages and methods to express, obtain, and organize proofs, (b) concerns developer practices and tools, (c) concerns issues such as mathematical foundations and choice of axioms, and (d) covers applications and consequences of proof engineering for mathematics and computer science.

## Proof Organization and Scalability

We describe specification languages (@Mulligan2014; @Sewell2010), proof languages (@Wenzel2015; @Corbineau2008), tactic languages (@Ziliani2015; @Malecha2016), specialized proof procedures (@Blanchette2016), constructs for organization and reuse (@Gonthier2011; @Sozeau2008), proof design principles (@Woos:2016:PCF:2854065.2854081; @Aydemir:2008:EFM:1328438.1328443), and higher-level frameworks (@Chlipala2013; @Nanevski2008).

## Practical Proof Development and Evolution

We consider user interfaces (@Aspinall2000; @Faithfull2016; @Roe2016), interface responsiveness features (@Barras2015; @Wenzel2014), user support features (@Komendantskaya2012; @Heras2013; @Whiteside2011), proof repair and evolution (@Roe2016; @Bobot2013), and proof development project processes and metrics (@Andronick_JKKSZZ_12; @Staples:2013:FSB:2486788.2486978; @Staples:2014:PPE:2652524.2652551).

## Reliability and Trusted Bases

We cover some foundations of proof assistants (@Barendregt2001; @pa-history-geuvers-sadhana09), their specific trust issues (@Pollack1998; @Wiedijk2012), approaches to certifying proof assistants themselves (@Barras2010; @Davis2015), and briefly the long-lived debate about the meaning and usefulness of formal proofs (@DeMillo1977; @Asperti2009; @Bringsjord2015).

## Technological and Social Impact

We describe case studies in program verification and formalized mathematics (@Kaestner2017; @Kumar2014; @Voevodsky2015; @Woos:2016:PCF:2854065.2854081) and how their usefulness can be measured by empirical means (@Bishop2005; @Yang2011), and finally prospects for future impactful research (@plse-coevolve-djg-fose14).

\bibliography{references}
