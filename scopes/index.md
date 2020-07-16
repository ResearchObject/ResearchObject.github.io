---
author: stain
date: 2015-07-20 15:59:20+00:00
layout: page
link: http://www.researchobject.org/scopes/
slug: scopes
title: Scopes
---

## Scopes and Profiles

[Research Objects](/overview/) can be used to capture academic outputs in a wide range of scopes, from detailed traces of software execution to consortium-wide results from a 5 year research project.

Research Object [extensions and serialization formats](/specifications/) can be applied together with domain-specific annotations to form a specific type of Research Object with a particular scope.

**Profiles** help define the shape and form of a domain- or application-specific research object. Loosely, a profile defines a **format** (e.g. Research Object Bundle), an expectation of **what kind of resources** should be expected, and link to any specific **vocabularies** or further specifications that should be used in its **annotations**. In a way, a profile defines the general **purpose** of that type of Research Objects, and documents what assumptions a consumer could rely on when processing such Research Objects.

A profile may mandate a [minimal information model](/initiative/mim/) checklist to formally specify its requirements, although the profile may just be a text document for a human reader.
Below is a list of known Research Object Profiles - feel free to [suggest](https://github.com/ResearchObject/researchobject.org/issues) changes to this list.

### Scientific Workflows

[Scientific workflows](https://en.wikipedia.org/wiki/Scientific_workflow_system) are computational experiments that are composed of a set of coordinated computational tasks, each of which takes some data inputs and produces some data outputs, which are then consumed by subsequent tasks according to the workflow definition, i.e. the experiment protocol definition. Scientific workflows provide the means for automating computational scientific experiments, enabled by established workflow execution engines, like [Apache Taverna](https://taverna.incubator.apache.org/), [Kepler](https://kepler-project.org/), [VisTrails](http://www.vistrails.org/) or [Galaxy](https://galaxyproject.org/).

A [workflow-centric research object](http://doi.org/10.1016/j.websem.2015.01.003) ([https://doi.org/10.1016/j.websem.2015.01.003](https://doi.org/10.1016/j.websem.2015.01.003)) contain the application-specific workflow definition, annotated with [wfdesc](http://purl.org/wf4ever/wfdesc), and combined with a [PROV](http://www.w3.org/TR/prov-o/)-based execution trace of one or more _workflow runs_, including _inputs_ and _outputs_. As an example of an application-specific profile, see Apache Taverna's [data bundle](https://github.com/apache/incubator-taverna-engine/tree/master/taverna-prov#structure-of-exported-provenance) from [TavernaProv](https://github.com/stain/2016-provweek-tavernaprov). ([https://doi.org/10.5281/zenodo.51314](https://doi.org/10.5281/zenodo.51314))

Building on that work, _CWLProv_ ([https://doi.org/10.5281/zenodo.1215611](https://doi.org/10.5281/zenodo.1215611)) is a recent development that extend the [reference implementation](https://github.com/common-workflow-language/cwltool) for the [Common Workflow Language](http://www.commonwl.org/) to capture workflow run provenance (what we can call _retrospective provenance_) using PROV, wfprov and [ro-bagit](https://w3id.org/ro/bagit) BDBags. Here the provenance capture rewrite the CWL workflow definition (which may have used local file paths) so it can be self-contained within the Research Object, and provide mechanisms for rerunning the workflow execution. As a vendor-neutral community project, CWL has [multiple implementations](https://www.commonwl.org/#Implementations) and relies on [Docker containers](https://www.docker.com/) and [BioConda](https://bioconda.github.io/) packages these Research Objects also achieve portability across platforms and workflow engines.

A slightly different workflow research object is aiming to capture just the _recipe_ for execution, what we can call a [plan](http://purl.org/net/p-plan) or [_prospective provenance._](http://workshops.inf.ed.ac.uk/tapp2015/TAPP15_III_3.pdf) Here the challenge is to provide all the required resources for executing the workflow, as well as history of the workflow definition itself. Early work in this area include [SCUFL2](https://www.escholar.manchester.ac.uk/item/?pid=uk-ac-man-scw:222016) Workflow Bundle, used by [Apache Taverna Language](https://taverna.incubator.apache.org/download/language/). More recently, in the [Common Workflow Language Viewer](https://view.commonwl.org), workflow definitions can be downloaded as a [Research Object Bundle](https://w3id.org/bundle) to capture runtime requirements of a CWL workflow, in addition to provenance of how the definition itself was created, [examining the corresponding GitHub log](https://doi.org/10.5281/zenodo.823295). ([https://doi.org/10.7490/f1000research.1114375.1](https://doi.org/10.7490/f1000research.1114375.1)).


### ISA model

The [ISA model](/initiative/isa/) (_Investigation/Study/Assay_) is commonly used in systems biology, life sciences, environmental and biomedical domains to structure research outputs. ISA defines a top-level _investigation_, consisting of _studies_, which contain several _assays_ (experiment or test) that produces _data_ files. In [SEEK for Science](http://seek4science.org/), used by the [FAIRDOM](http://fair-dom.org/) data management project, a complete investigation can be downloaded as a Research Object Bundle, which is structured according to the ISA model to include all contained resources and their annotations. These research objects corresponds to temporal _snapshots_ of the whole investigation and its resources, which can be [assigned DOIs](http://docs.seek4science.org/help/user-guide/investigation-snapshots.html#assigning-a-doi) like [https://doi.org/10.15490/fairdomhub.1.investigation.162.1](https://doi.org/10.15490/fairdomhub.1.investigation.162.1) - from where you can download the [corresponding Research Object Bundle](https://fairdomhub.org/investigations/162/snapshots/1/download).

The [SOAPdenovo2 reproducibility study](http://isa-tools.github.io/soapdenovo2/) ([https://doi.org/10.1371/journal.pone.0127612](https://doi.org/10.1371/journal.pone.0127612)) showed how to recreate a scientific workflow (using [Galaxy](https://galaxyproject.org/)) of the original [SOAPdenovo2 paper ](https://doi.org/10.1186/2047-217X-1-18)using a combination of the [ISA model](http://isacommons.org/), [Nanopublication](http://nanopub.org/), and [Research Object](http://www.researchobject.org/) (RO). As the resulting [dataset](https://doi.org/10.5524/100148) ([https://doi.org/10.5524/100148](https://doi.org/10.5524/100148)) includes all of these serializations they can be compared for completeness and complexity.


### Digital Preservation

In digital libraries, preservation of source artifacts commonly use the [BagIt](https://en.wikipedia.org/wiki/BagIt) format for archive serialization, capturing digital resources like audio recordings, document scans and their transcriptions, provenance and annotations. The [Research Object BagIt archive](https://w3id.org/ro/bagit) is a profile for describing a BagIt archive and its content as a Research Object to structure the metadata and relate the captured resources, used by the NIH-funded [Big Data for Discovery Science](http://bd2k.ini.usc.edu/) (BDDS) project to capture [Big Data bags](https://static.aminer.org/pdf/fa/bigdata2016/BigD418.pdf) (BDBag) of large complex datasets from genomics workflows. BDDS also developed the the [bdbag ](http://bd2k.ini.usc.edu/tools/bdbag/)utility and Python library to create/inspect/manipulate such research objects. ([https://doi.org/10.1109/BigData.2016.7840618](https://doi.org/10.1109/BigData.2016.7840618)).

A key aspect of BDBag is the ability to use _Minimal Viable Identifiers_ ([minid](http://minid.bd2k.org/)) for referencing potentially large data sources held in multiple remote repositories, effectively making a "Big Data" Research Object for large-scale workflows ([https://doi.org/10.1101/268755](https://doi.org/10.1101/268755)).   A _bag of bags_ ([minid:b9vx04](<a href=)) may look tiny at 182 kB, but it is a metadata skeleton which may be completed with tools like [bdbag](http://bd2k.ini.usc.edu/tools/bdbag/) to download the big data using efficient methods like [GridFTP](http://toolkit.globus.org/toolkit/docs/latest-stable/gridftp/) from alternative repositories, confirming cryptographically strong hashes against BagIt manifests. Alternatively, the bags' Research Object manifests can be consumed independently, linking to the remote resources. Further work on BDBags is taking place as part of [NIH Data Commons](http://www.researchobject.org/2017-12-commonspilot/).


### Simulation Experiments

A simulation study usually consists of multiple modules. A _computational model_ describes a real-world system, a _simulation description_ defines the parametrisation, and some _documentation_ explains how to use and run the study. The experiment can then be simulated in silico to study the behaviour under different conditions. This approach helps understanding the encoded system and allows for making predictions about what will happen in the real system without spending money and time for wet lab experiments.

A simulation object (which is a research object encoding for a simulation experiment) needs to contain all files necessary to reproduce the results of a certain simulation experiment. It must be annotated with the information about the creators and authors of the files/modules shipped with the study. Moreover, it should make use of standard formats (such as SBML, CellML, SED-ML) as far as possible. See also [COMBINE Archive](/initiative/combine-archive/) ([https://doi.org/10.1186/s12859-014-0369-z](https://doi.org/10.1186/s12859-014-0369-z)).


### Computational Jobs

The [STELAR project](/initiative/stelar/) uses research objects as part of its computational job management, by capturing analysis code in a _Snapshot Research Object_, and submitting a _Job Research Objects_ that aggregate all of the content required to execute the analysis code, e.g. the Snapshot Research Object and input data files. _Annotations_ included metadata required for execution: command line parameters, environment variables and the necessary computational resources (e.g. CPU and memory). Results are returned as _Execution Research Objects_ that aggregates the Job Research Object along with the outputs of the process: output files, standard input, standard output and standard error. ([https://doi.org/10.1136/thoraxjnl-2015-206781](https://doi.org/10.1136/thoraxjnl-2015-206781))


### Health Informatics


For sharing Public Health datasets within the [Farr institute of Health Informatics research](http://www.farrinstitute.org/) ([https://doi.org/10.17061/phrp2541541](https://doi.org/10.17061/phrp2541541)), the [Farr Commons](http://farrcommons.github.io/) defines a Research Object profile with a series of requirements on _identifiers_, _versioning_ and _licensing_ of datasets. Availability aspects include _privacy_ regulations, and domain-specific annotations include _cohort_ and [clinical codes](/initiative/clinicalcodes/).


### Regulatory Science


[BioCompute Objects](https://doi.org/10.17605/osf.io/h59uh) (BCO) is a community-driven project [backed by the FDA](https://www.fda.gov/ScienceResearch/SpecialTopics/RegulatoryScience/ucm491893.htm) (US Food and Drug Administration) and [George Washington University](https://hive.biochemistry.gwu.edu/home) to standardize exchange of High-Troughput-Sequencing workflows for regulatory submissions between FDA, pharma, bioinformatics platform providers and researchers. ([https://doi.org/10.1101/191783](https://doi.org/10.1101/191783))

There is a particular challenge for regulatory bodies like [FDA](https://www.fda.gov/) in areas like personalized medicine, as to review and approve the bioinformatics side they need to _inspect_ and in some cases _replicate_ the computational analytical workflow.  The challenge here is not just the normal reproducibility thing about _packaging_ software and providing required _datasets_, but also for _human understanding_ of what has been done, by expressing the higher level steps of the workflow, their _parameter_ spaces and _algorithm_ settings.

To this end, the [Research Objects complements the BioCompute Object,](http://www.researchobject.org/2017-11-27-biocompute-objects/) as the RO captures aggregation, provenance and attribution; while the BCO captures domain-specific aspects. We are [exploring](http://slides.com/soilandreyes/2018-03-23-bco-cwl-ro#/) this approach using the [ELIXIR](https://www.elixir-europe.org/) implementation study [Enabling the reuse, extension, scaling, and reproducibility of scientific workflows](https://www.elixir-europe.org/about-us/implementation-studies/cwl-2018).




