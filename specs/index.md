---
author: Matt
date: 2014-03-03 13:38:16+00:00
layout: page
link: http://www.researchobject.org/specifications/
slug: specifications
title: Specs & Tooling
---


## Specifications and Tooling

<div class="alert alert-info" role="alert">
  It is <strong>recommended</strong> that new Research Object users adapt the <a href="/ro-crate/">RO-Crate</a> specification.
</div>


### Research Object Crate



[RO-Crate](/ro-crate/) is a community effort to establish a lightweight
approach to packaging research data with their metadata. It is based on
[schema.org](https://schema.org/) annotations in
[JSON-LD](https://json-ld.org/), and aims to make best-practice in formal
metadata description accessible and practical for use in a wider variety of
situations, from an individual researcher working with a folder of data, to
large data-intensive computational research environments.

RO-Crate is the marriage of _Research Objects_ with
[DataCrate](https://github.com/UTS-eResearch/datacrate). It aims to build on
their respective strengths, but also to draw on lessons learned from those
projects and similar research data packaging efforts. For more details, see
[RO-Crate background](/ro-crate/background/).

The [RO-Crate specification](https://w3id.org/ro/crate/1.1) details how to
capture a set of files and resources as a dataset with associated metadata –
including contextual entities like people, organizations, publishers, funding,
licensing, provenance, workflows, geographical places, subjects and
repositories.

A growing list of [RO-Crate tools and libraries](/ro-crate/implementations.html)
simplify creation and consumption of RO-Crates, including the graphical
interface [Describo](https://uts-eresearch.github.io/describo/).

Join the [RO-Crate community](/ro-crate/community.html) to help shape the
specification or get help with using it!


### Research Object Model specifications

<div class="alert alert-warning" role="alert">
  <strong>Note</strong>: The legacy specifications for the <em>Research Object Model</em> 
    (below) are no longer actively maintained. It is
    <strong>recommended</strong> that new users of Research Object adapt 
    <a href="/ro-crate/">RO-Crate</a>.
</div>


#### RO core

<div class="alert alert-info" role="alert">
  Latest Research Object Model release is: 
  <a href="https://w3id.org/ro/2016-01-28">2016-01-28</a>
</div>

 * [ro overview](https://w3id.org/ro/2016-01-28/) - Overview of the Research Object Model vocabularies
 * [ro ontology](https://w3id.org/ro/2016-01-28/ro) - The core concepts of Research Objects, identity, aggregation, and annotation, are captured in the specification of the _ro model_. The specification of this core Research Object model is described in the _ro_ ontology under the namespace [http://purl.org/wf4ever/ro#](http://purl.org/wf4ever/ro#).
 * [ro-bundle](https://w3id.org/bundle) - Research Object Bundle, a zip-based serialization of the Research Object model based upon the Adobe Universal Container Format (UCF).
 * [bagit-ro](https://w3id.org/ro/bagit) - A profile for Research Object as [BagIt archives](https://tools.ietf.org/html/draft-kunze-bagit-14), which can be serialized as _zip_, _tar_ or _tar.gz _- basis for [BDBag](https://github.com/fair-research/bdbag) (_Big Data Bags_) developed by [FAIR Research](https://fair-research.org).
 * [LDP4ROs](http://purl.org/net/ldp4ro/spec) - Alignment between the Research Object model and the W3C [Linked Data Platform](http://www.w3.org/TR/ldp/) (LDP).


#### RO extensions

We know of the following ontology extensions to the core Research Object model:
	
 * [roevo](https://w3id.org/ro/2016-01-28/roevo) model describing the evolution of a Research Object and its aggregated resources, which is also based on the [W3C PROV Ontology](http://www.w3.org/ns/prov#) recommendation
 * [wfprov](https://w3id.org/ro/2016-01-28/wfprov) provenance model describing the execution of a scientific workflow, which is based on the latest [W3C PROV Ontology](http://www.w3.org/ns/prov#) recommendation.
 * [wfdesc](https://w3id.org/ro/2016-01-28/wfdesc) model describing scientific workflow protocols to facilitate interpretation and reuse of scientific workflow
 * [wf4ever](https://w3id.org/ro/2016-01-28/wf4ever) model describes common workflow service types and properties
 * [RO-Opt](http://purl.org/net/RO-optimization#) ontology is designed for representing optimizations done to workflows and their provenance
 * [roterms](https://w3id.org/ro/2016-01-28/roterms) vocabulary defines terms useful for typing and annotation of resources in a Research Object, e.g. _Hypothesis_, _ExampleRun_, _technicalContact_, _exampleValue_
 * [MINIM minimum information model](http://purl.org/minim/description) for defining checklists for Research Objects. A Minim model defines a list of MUST/SHOULD/MAY requirements, associated with rules that express how to satisfy the requirement, e.g. by requiring certain resources to exist in the RO, or a more detailed query that must be fulfilled in its annotations.


### RO Model tooling


 * [ROHub](http://www.rohub.org/) - a web application for creating, sharing and inspecting Research Objects.
 * [bdbag ](https://github.com/ini-bdds/bdbag)- a **Python** library and command line for creating and manipulating [bagit-ro ](https://w3id.org/ro/bagit)archives
 * [ro-python](https://github.com/ResearchObject/ro-python) - a **Python** library and command line to create/modify/inspect research object directories and RO Bundles - based on _RO Manager_
 * [RO Manager](https://github.com/wf4ever/ro-manager) - A git-like command-line tool that can be used create research objects in your local file directory.
 * [RO bundle API](https://github.com/apache/incubator-taverna-language/tree/master/taverna-robundle) - A **Java** library that can be used to generate and inspect the zip-based Research Object Bundles archives and their metadata.
 * [ruby-ro-bundle](https://github.com/myGrid/ruby-ro-bundle) - a **Ruby** library for creating/inspecting Research Object Bundles and their metadata.
 * [Combine archive conversion](https://github.com/stain/ro-combine-archive) - A tool for converting a [COMBINE archive](http://co.mbine.org/documents/archive) into a RO bundle, and vice versa. COMBINE archives can be browsed and modified using [CombineArchiveWeb](http://cat.sems.uni-rostock.de/).
 * [Latex2RO](https://github.com/dgarijo/Latex2RO) - A simple tool designed to help creating Research Objects (ROs) from LaTeX papers. Given a LaTeX file, the RO creator will extract its title and metadata and fill partially a structured HTML page annotated in RDF-a with these metadata.
 * [LDP4RO](https://github.com/oeg-upm/LDP4RO) - A [LDP4J](https://github.com/oeg-upm/LDP4RO) extension for creating, accessing and browsing Research Objects. See also the [LDP4RO demo](http://purl.org/net/ldp4ro).
 * [ro-show](https://github.com/ResearchObject/ro-show) - a web application for viewing Research Objects (under development)


### RO Model tutorials

[Research Object Ontologies and Vocabularies Primer](http://purl.org/wf4ever/ro-primer) introduces the Research Object model and ontology, using an example of a Workflow Research Object described as Linked Data.

[Research Object Tutorials](https://github.com/researchobject/ro-tutorials) provide a step-to-step example of creating a [Research Object bundle](https://w3id.org/bundle), explaining the bundle structure and manifest.


