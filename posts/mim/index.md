author: Matt
date: 2014-08-07 16:32:22+00:00
layout: page
link: http://www.researchobject.org/initiative/mim/
slug: mim
title: Minimum Information Model
tags:
- Checklists
- Description
- Linked Data
- Machine Readable
- mim
- minim
- RDF
- vocabulary
---
Minimum Information Checklists (MICs) exist primarily in the Life Sciences as a means of describing a required set of data and metadata in the reporting of a particular class of experiment or type of data. The [Biosharing](http://biosharing.org/) initiative for example currently lists 60+ checklists detailing the report requirements for wide array of Biological experimental data. The motivation for defining a MIC is to improve the quality of the reported data, ensure that set of metadata is sufficient for the data to be unambiguously interpreted, and maximise the potential for reuse. The motivation for creating a vocabulary is to support the use of MICs in the Web of Data.
University of Manchester developed the [MIM (Minimum Information Model Vocabulary)](https://github.com/ResearchObject/mim-vocabulary) to provide a meta-modelling vocabulary suitable to encoding MICs in machine readable RDF. By allowing others to describe a MIC that is specific to some class of data, the goal of MIM is to have a library of RDF encoded checklists as community-resources published as Linked Data. MIM formed the basis for MINIM.
[MINIM](http://purl.org/minim/description) is a model for defining checklists for Research Objects. A Minim model defines a list of MUST/SHOULD/MAY requirements, associated with rules that express how to satisfy the requirement, e.g. by requiring certain resources to exist in the RO, or a more detailed query that must be fulfilled in its annotations.
