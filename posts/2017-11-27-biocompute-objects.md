author: stain
date: 2017-11-09 15:25:46+00:00
link: http://www.researchobject.org/2017-11-27-biocompute-objects/
slug: 2017-11-27-biocompute-objects
title: 2017-11-27 BioCompute Objects
categories:
- Event
- News
tags:
- bagit
- bco
- cwl
- fda
---
[BioCompute Objects](https://doi.org/10.17605/osf.io/h59uh) (BCO) is a community-driven project [backed by the FDA](https://www.fda.gov/ScienceResearch/SpecialTopics/RegulatoryScience/ucm491893.htm) (US Food and Drug Administration) and [George Washington University](https://hive.biochemistry.gwu.edu/home) to standardize exchange of High-Throughput-Sequencing workflows for regulatory submissions between FDA, pharma, bioinformatics platform providers and researchers.
[![BioCompute Objects](http://www.researchobject.org/pages/wp-content/uploads/2013/06/BCO-logo.png)](https://osf.io/h59uh/)
Members of the Research Object team ([Carole Goble](http://orcid.org/0000-0003-1219-2137), [Stian Soiland-Reyes](http://orcid.org/0000-0001-9842-9718), [Michael R Crusoe](http://orcid.org/0000-0002-2961-9670)) have been collaborating closely with the rest of the BCO community since 2016, in particular covering the integration of BCO with existing standards like [Research Object](http://www.researchobject.org/specifications/), [W3C PROV](https://www.w3.org/TR/prov-overview/) and [Common Workflow Language](http://www.commonwl.org/).
[Vahan Simonyan](https://www.linkedin.com/in/vahan-simonyan-a6a65723) from FDA [presented](http://www.signupgenius.com/go/30e044da4ab2ea2fb6-sign) BioCompute Objects to the [GA4GH Cloud](http://ga4gh.cloud) workstream webinar on **2017-11-27**. 
The below blog post is based on an extract of [Vahan's slides](https://osf.io/zks4w/) modulated to cover my thoughts on the role of Research Objects with BCOs.
<!-- more -->



  
  * Introduction

  
  * Model of BioCompute Objects

  
  * JSON of BioCompute Object

  
  * Links and references

  
  * Packaging it up: Research Object

  
  * Take part!




## Introduction


There is a particular challenge for regulatory bodies like [FDA](https://www.fda.gov/) in areas like [personalized medicine](https://www.fda.gov/downloads/ScienceResearch/SpecialTopics/PersonalizedMedicine/UCM372421.pdf), as to review and approve the bioinformatics side they need to _inspect_ and in some cases _replicate_ the computational analytical workflow.  The challenge here is not just the normal [reproducibility](https://doi.org/10.1016/j.future.2017.01.012) thing about _packaging_ software and providing required _datasets_, but also for _human understanding_ of what has been done, by expressing the higher level steps of the workflow, their _parameter_ spaces and _algorithm_ settings.​ ([PMC5510742](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5510742/))


## Model of BioCompute Objects


At the heart of the BCO is a domain-specific object model which capture this essential information without going in details of the actual execution:
[![BioCompute Object](http://www.researchobject.org/pages/wp-content/uploads/2017/11/bco-example-transparent.png)](http://www.researchobject.org/pages/wp-content/uploads/2017/11/bco-example-transparent.png)
The full background and development of the BioCompute Object model is detailed in the recent BCO community paper ([https://doi.org/10.1101/191783](https://doi.org/10.1101/191783)).


## JSON of BioCompute Object


The BCO is expressed as a [JSON](http://www.json.org/) format, which also includes additional metadata and external identifiers.​
[![BioCompute Object as JSON](http://www.researchobject.org/pages/wp-content/uploads/2017/11/bco-json.png)](http://www.researchobject.org/pages/wp-content/uploads/2017/11/bco-json.png)
If we look at this JSON briefly, it is split into _metadata_, a brief overview of the _pipeline_ with _arguments_ and _scripts_. The actual _workflow definition_ is defined outside. In addition we define _parametric domain,_ and for verification the _input/output domains_. This allows inspection to see what is the _scope_ of the analysis.​ For more details, see the first release of the [BCO Specification](https://osf.io/zm97b/) Document ([https://osf.io/zm97b/](https://osf.io/zm97b/)).


## Links and references


Looking deeper, many of the BioCompute entries are actually external links or references: ​​ [![Embedded and external references within BCO JSON](http://www.researchobject.org/pages/wp-content/uploads/2017/11/2017-10-18-bco-ro-2.svg)](http://www.researchobject.org/pages/wp-content/uploads/2017/11/2017-10-18-bco-ro-2.svg)
The authors and contributors are identified using [ORCID](https://orcid.org/), which is a de-facto standard identifier for researchers.
The cross-references are provided with [identifiers.org](http://identifiers.org/) prefixes.
The pipeline can be provided in any language, like [Python​](https://www.python.org/), or it be specified using [Common Workflow Language](http://www.commonwl.org/) – which gives portability as well as capturing execution environment, e.g. which Python version to use for the scripts.​
The referenced data files are of course in multiple formats, like CSV or – for sequencing data - more specific formats like [SAM​](https://samtools.github.io/hts-specs/SAMv1.pdf).
​Now while the BCO references these resources in several places in its JSON structure, some may also be indirectly referenced. For instance the CWL workflow might reference particular [Docker](http://docker.com/) images that capture the Python version to use. ​
[W3C PROV](https://www.w3.org/TR/prov-overview/) files might be provided, which can explain more detailed provenance of workflows (e.g. using [wfprov](https://w3id.org/ro/2016-01-28/wfprov)); this might however become specific to the workflow engine used, and might not be directly identified all the resources seen in the BCO. ​
While we can identify authors with ORCID, they might author _different parts_ of the BCO. If you made a clever Python script used by a BCO, then it is only [FAIR](https://doi.org/10.1038/sdata.2016.18) that you should be attributed – even if you were nowhere in the vicinity when the BCO was later created.​
So let's have a look at all the direct and indirect links:
[![Implicit and explicit references from BCO](http://www.researchobject.org/pages/wp-content/uploads/2017/11/2017-10-18-bco-ro-arrows.svg)](http://www.researchobject.org/pages/wp-content/uploads/2017/11/2017-10-18-bco-ro-arrows.svg)
So you can think of the pink, green and blue arrows in the figure above as each giving partial picture of what is the whole BioCompute Objects.​


## Packaging it up: Research Object


So we've identified that there are multiple _references, attributions_, _provenance_ traces and _annotations_ to keep track of in a BioCompute Object.
There is also the question of how to **move** the BCO around – the JSON has many external references as well as relative references to plain files – how can you capture it all without understanding all of the BCO spec?​
We are looking at using the [BagIt Research Objects](http://www.researchobject.org/bagit-for-transferring-and-archiving-research-objects/) for this purpose. ​
[Bag-It is](https://tools.ietf.org/html/draft-kunze-bagit-14) a digital archive format used by Library of Congress and digital repositories. It handles checksums and completeness of files, even if they are large or external. ​
[Research Object](http://www.researchobject.org/) (RO) ([https://doi.org/10.1016/j.websem.2015.01.003](https://doi.org/10.1016/j.websem.2015.01.003)) is a model for capturing and describing research outputs; embedding data, executables, publications, metadata, provenance and annotations. Although it is a general model, ROs have been used in particular for capturing reproducible workflows.​
The combination of these, [ro-bagit](https://w3id.org/ro/bagit) aka [BDBags](http://bd2k.ini.usc.edu/tools/bdbag/) has recently been used by the [NIH-BD2K](https://commonfund.nih.gov/bd2k)-funded [BDDS](http://bd2k.ini.usc.edu/) project for transferring and archiving very large HTS datasets ([https://doi.org/10.1109/BigData.2016.7840618](https://osf.io/zm97b/) [[preprint](https://static.aminer.org/pdf/fa/bigdata2016/BigD418.pdf)]) in a location-independent way (the BDDS group has recently been [awarded new funding](https://ci.uchicago.edu/press-releases/two-uchicago-groups-join-nih-biomedical-data-sharing-cloud-pilot) under [NIH Data Commons](https://commonfund.nih.gov/bd2k/commons)), so we hope BDBags could be a good choice also to to package and archive BCOs.​
The below figure illustrates how the manifest of the Research Object (_manifest.json_) ties the BioCompute Object together:
[![RO manifest aggregating the complete BCO](http://www.researchobject.org/pages/wp-content/uploads/2017/11/2017-10-18-bco-ro-3.svg)](http://www.researchobject.org/pages/wp-content/uploads/2017/11/2017-10-18-bco-ro-3.svg)
The [Research Object manifest](https://w3id.org/bundle#manifest) ([https://doi.org/10.5281/zenodo.12586](https://doi.org/10.5281/zenodo.12586)) is in [JSON-LD](https://json-ld.org/) format – so it is [Linked Data](https://www.w3.org/standards/semanticweb/data) – but you don’t have to know unless you really want to – for everyone else it just JSON.​
The manifest **aggregates** all the other resources, including the BCO, but also external resources as well as outside references like [identifiers.org](http://identifiers.org/). ​
The aggregation also provide _attribution_ and _provenance_ of each resource, so they get the credit they deserve. This is of course also important for regulatory purposes, e.g. to check if the latest version of a tool was used.​
An important aspect of research objects is also to capture annotations, using the [W3C Web Annotation Model](https://www.w3.org/TR/annotation-model/). This allows any part of the BCO to be further described; textually or semantically; so you are not limited to what is supported by the specification of BCO or Research Object. In particular this might be where community-driven standards like [BioSchemas](http://bioschemas.org/) can be used.​
[![BCO RO logo soup](http://www.researchobject.org/pages/wp-content/uploads/2017/11/2017-10-18-bco-ro-4.svg)](http://www.researchobject.org/pages/wp-content/uploads/2017/11/2017-10-18-bco-ro-4.svg)
So to finish off with a Logo Soup™ – while BioCompute Objects are developed with domain-specific requirements in mind, and in a way is “[yet another standard](https://xkcd.com/927/)” – it is also fitting into a landscape of well-established standards, technologies and communities.​
In particular our [BCO team](https://osf.io/h59uh/) includes people who are or have also worked on [Common Workflow Language](http://www.commonwl.org/), [Research Object](http://www.researchobject.org/), [BioSchemas](http://bioschemas.org/), [ORCID](https://orcid.org/), [PROV](https://www.w3.org/TR/prov-overview/) and [GA4GH](https://www.ga4gh.org/). ​
So we’re not developing BCO in isolation, but with these integrations and collaboration as pragmatic parts of our future direction.​


## Take part!


Do you want to take part in shaping Biocompute Objects? See the [BioCompute Project Space at Open Science Framework](https://osf.io/h59uh/), or join our community WebEx meetings (for call details, contact Charles Hadley King at: [hadley_king@gwu.edu](mailto:hadley_king@gwu.edu))
