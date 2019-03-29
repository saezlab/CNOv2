# CNOv2

Main repository for the new CellNOpt features (CNOv2).

Codes for each of the new features should be added to the corresponding directory in */Features/R/*. Codes should be well documented and accompanied with a description and an example in the *README.md*.

## License

Since the new codes will be added to the CellNOptR package, for consistency we place the license agreement as the header of each *R* function as for example:

```R
#
#  This file is part of the CNO software
#
#  Copyright (c) 2019-2020 - Bioquant - Heidelberg University
#
#  File author(s): Enio Gjerga (cellnopt-developers@googlegroups.com)
#
#  Distributed under the GPLv3 License.
#  See accompanying file LICENSE.txt or copy at
#      http://www.gnu.org/licenses/gpl-3.0.html
#
#  CNO website: http://www.cellnopt.org
#
##############################################################################
# $Id$
```

## Documentation

The documentation of each function should contain a description of the tasks accomplished by each function, inputs and outputs object. Documentation is to be written with *Roxygen2*. The subdirectory */Features/man/* should be containing a set of files, one per function, in a special R Documentation format (.Rd). These will be the source for the documentation for each function; R processes them to create plain text, PDF, and HTML versions.

## Tasks

Each contributor in this repository is responsible for uploading, documenting and maintaining the function scripts of each new features. The tasks assigned are:

* **1)** CellNOpt-ILP (Enio)
** **a)** Rationale (faster, guaranteed best solution, multiple best models)
** **b)** Formulation (maybe in the supplementary materials? + modifications from the original Mitsos formulation)
** **c)** Simple case-study (phospho-proteomics data generated in the liver cancer cell line HepG2 - applied in [*Mitsos et.al.*](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1000591) and [*Guziolowski et.al.*](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3753570/))

* **2)** Dynamic-Feeder (Enio)
** **a)** Rationale (further refinement of the PKN, feeder for the boolean CNO + CNORode)
** **b)** Workflow (enrichment of the curated PKN with possible interactions from other databases, different metrics (MI, mse), a data driven component to infer other possible interactions not present in the PKN or the database)
** **c)** Interactions from Omnipath → weights
** **d)** Simple case-study (HPN-DREAM breast cancer phosphoproteomic data)

* **3)** CNORProb (Panuwat)
** **a)** Probabilistic framework (Probabilistic Boolean/Bayesian networks) vs Fuzzy logic network
** **b)** Alternative pipeline to CNORfuzzy for quantitative optimisation of steady-data 
** **c)** Interpretation of results based on edges’ probability
** **d)** (optional) point out different formulation for logical gates + additive effect between CNO and FALCON/CNOprob
** **e)** Simple case-study (TBD)

* **4)** Plotting & New Cytocopter (Attila + Francesco)
** **a)** SBML-Qual in/out
** **b)** The new plotting features - RMSE on plot fit 

* **5)** CellNOpt-Maboss (Aurelien)
** **a)** Asynchronous boolean framework with Gillespi algorithm for approximation
** **b)** Bounded continuous outputs 
** **c)** Cyclic attractors and negative feedbacks

* **6)** Post-hoc systematic analyses (Attila, Panuwat)
** **a)** Bootstrapping: Boolean, prob, ode
** **b)** Cross-validation: boolean
** **c)** Sensitivity analyses
** **d)** Edge/Node Knock-out analyses

## Targeted Journals

* Application Note in Bioinformatics (2 pages, 1 figure)
* BMC bioinformatics/systems biology
