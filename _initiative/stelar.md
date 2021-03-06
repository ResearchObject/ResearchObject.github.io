---
author: stain
date: 2015-11-06 10:00:23+00:00
layout: page
link: http://www.researchobject.org/initiative/stelar/
slug: stelar
title: STELAR Asthma e-Lab
tags:
  - Annotations
  - Execution
  - Health Informatics
  - Reproducibility
  - Research Object
---
The [STELAR project](http://www.population-health.manchester.ac.uk/healthinformatics/research/STELAR/)
developed the _Asthma-e-Lab_, an application of the [HeRC e-Lab
platform](http://www.herc.ac.uk/2015/05/27/e-lab-the-home-of-team-science/),
bringing together Clinicians, Health Informaticians, Statisticians and Data
Managers to establish an improved understanding of early life asthma. There is
growing evidence to suggest that asthma is an umbrella diagnosis that includes
multiple diseases with different underlying mechanisms. It is thought to be
unlikely that these different diseases will respond in the same way to
therapeutic treatments. The aim of the STELAR project was to perform a
statistical analysis across data gathered as part of multiple UK based _birth
cohort studies_ to identify clusters of characteristics (or _phenotypes_) of
asthma that may in turn relate to specific _endotypes_. Identification of these
endotypes may then support an improved stratified approach to the treatment of
individuals with the disease.

The _e-Lab platform_ can be used to create collaboration spaces that can be
accessed in a straightforward manner using a standard web browser. These spaces
can be tailored for specific teams, making available tools that include those
to manage documents, wikis and blogs and provide social networking capability.
e-Labs offer a standard set of tools that can be incorporated into these
spaces, but also implement an architecture that allows new software components
to be easily incorporated. Users are able to create sharable snapshots of the
collaboration space that include detailed metadata about individual content and
the relationships between content. These snapshots are managed as 
[Research Object Bundles](https://w3id.org/bundle/) and provide an important mechanism
for _aggregating, identifying and annotating_ sharable content.

The _Variable Manager_ module has been developed to allow the integration of
data sets gathered across the five birth cohort studies. These data sets can be
imported into the e-Lab and associated with a _data description_. The
descriptions are developed by the data managers of the cohorts and provide
detailed information about the imported data. This includes information about
how data are represented, the semantics and additional context required for
correct interpretation. These data sets can then be integrated in a manner that
allows research questions to be asked across multiple data sets, created by
different communities. Data are stored in a domain-independent way such that
the software can be easily extended and applied in different contexts.

The _Job Manager_ module supports reproducibility of the research findings of
STELAR, allowing users to capture research processes in a manner that enables
their repetition. Analysis code can be uploaded to the e-Lab and captured in a
**Snapshot Research Object**. The user can then create **Job Research Objects**
that aggregate all of the content required to execute the analysis code, for
example the Snapshot Research Object and input data files. _Annotations_
included in the Job Research Object provide the metadata required for
execution, including command line parameters, environment variables and the
necessary computational resources (e.g. CPU and memory). 

The Job Manager can be used to manage the execution of Job Research Objects on
compute resources, including moving code and input files to a remote resource,
providing the status of processes and moving output files back into the e-Lab.
Each completed execution is captured as an **Execution Research Object** that
aggregates the Job Research Object along with the outputs of the process,
including output files, standard input, standard output and standard error. The
e-Lab can be used to publish Execution Research Objects, associating them with
a DOI that can be used to reference the Research Object in publications.

