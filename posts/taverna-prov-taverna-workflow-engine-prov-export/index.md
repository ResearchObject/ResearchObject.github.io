author: Matt
date: 2014-08-08 09:31:28+00:00
layout: page
link: http://www.researchobject.org/initiative/taverna-prov-taverna-workflow-engine-prov-export/
slug: taverna-prov-taverna-workflow-engine-prov-export
title: 'taverna-prov: Taverna Workflow Engine Prov Export'
tags:
- Aggregation
- Annotation
- Exchange
- Identity
- Provenance
- RO Bundle
- ZIP
---
Taverna-prov is a plugin for the [Taverna](http://www.taverna.org.uk/) Workbench and Taverna Command Line - a scientific workflow engine. The plugin allows the export of the provenance of a workflow run according to the [W3C PROV-O standard](http://www.w3.org/TR/prov-o/).
The provenance is exported as a `.bundle.zip` file  which species a structured ZIP file with a manifest (`.ro/manifest.json`) that corresponds to the [RO bundle](https://w3id.org/bundle) specification.
The following is an [example bundle](https://github.com/taverna/taverna-prov/blob/master/example/helloanyone.bundle.zip) and [unzipped bundle](https://github.com/taverna/taverna-prov/blob/master/example/helloanyone.bundle) as a folder. This data bundle has been saved after running a simple [hello world workflow](https://github.com/taverna/taverna-prov/blob/master/example/helloanyone.t2flow).
