---
title: "Should the choice of BOIN design parameter p.tox only depend on the target DLT rate?"
collection: publications
permalink: /publication/2024-02-17-paper-title-number-4
excerpt: 'This study demonstrates the importance of interpreting BOIN design parameter p.tox as an interval of toxicity rates that are considered too toxic, rather than one prespecified value that corresponds to the lowest toxicity probability that is deemed overly toxic. When designing a dose-finding trial using BOIN, it is important to perform simulation studies to identify equivalent sets of BOIN design parameters that can generate the same boundary table so that we can better compare the safety properties of different boundary tables. '
date: 2024-01-28
venue: 'GitHub'
paperurl: 'http://ronglu-stanford.github.io/files/paper_28Jan2024.pdf'
citation: 'Rong Lu (2024). &quot;Should the choice of BOIN design parameter p.tox only depend on the target DLT rate?&quot; <i>GitHub</i>. http://ronglu-stanford.github.io/files/paper_28Jan2024.pdf.'
---

**Abstract:**

**IMPORTANCE:** On December 10, 2021, the FDA published a [Determination Letter](https://www.fda.gov/media/155363/download?attachment), along with a [Statistical Review and Evaluation Report](https://www.fda.gov/media/155364/download?attachment), and concluded that under the non-informative prior, the local Bayesian optimal interval design (BOIN) design, in its revised form, can be designated fit-for-purpose for identifying the maximum tolerated dose of a new drug, assuming that dose-toxicity relationship is monotonically increasing. Although setting the BOIN design parameter _p.tox_ = 1.4 \* _target.DLT.rate_ is recommended in almost all BOIN methodology articles and is the default value in the R package _BOIN_, it’s unclear if the choice of _p.tox_ should only depend on the target DLT rate and if certain range of _p.tox_ could produce the same BOIN boundary table.

**DESIGN:** In this simulation study, following parameters were varied one at a time, using R package _BOIN_, to explore their effects on the equivalence intervals of _p.saf_ and _p.tox_: 1) target DLT rate, 2) _n.earlystop_, 3) _cutoff.eli_, 4) _cohortsize_, and 5) _ncohort_. And a simple 3+3 design was used as an example to explore equivalent sets of BOIN design parameters that can generate the same boundary table.

**RESULTS:** When the early stopping parameter _n.earlystop_ is relatively small or the cohortsize value is not optimized via simulation, it might be better to use _p.tox_ < 1.4 \* _target.DLT.rate,_ or try out different cohort sizes_,_ or increase _n.earlystop_, whichever is both feasible and provides better operating characteristics. This is because if the _cohortsize_ was not optimized via simulation, even when _n.earlystop_ = 12 and _cohortsize_ > 3, the BOIN escalation/de-escalation rules generated using _p.tox_ = 1.4 \* _target.DLT.rate_ could be exactly the same as those calculated using _p.tox_ > 3 \* _target.DLT.rate_, which might not be acceptable for some pediatric trials targeting 10% DLT rate.

The traditional 3+3 design stops the dose finding process when 3 patients have been treated at the current dose level, 0 DLT has been observed, and the next higher dose has already been eliminated. If additional 3 patients were required to be treated at the current dose in the situation described above, the decision rules of this commonly used 3+3 design could be generated using BOIN design with target DLT rates ranging from 18% to 29%, _p.saf_ ranging from 8% to 26%, and different _p.tox_ values ranging from 39% to 99%. These BOIN parameters also need to satisfy a set of conditions.

**_Acknowledgement:_** _This work is partially supported by the Biostatistics Shared Resource (BSR) of the NIH-funded Stanford Cancer Institute (P30CA124435) and the Stanford Center for Clinical and Translational Research and Education (UL1-TR003142). The funders had no role in the design and conduct of the study; collection, management, analysis, and interpretation of the data; preparation, review, or approval of this abstract._

