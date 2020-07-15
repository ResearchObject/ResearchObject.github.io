---
author: stain
date: 2015-07-17 15:54:24+00:00
link: http://www.researchobject.org/bagit-for-transferring-and-archiving-research-objects/
slug: bagit-for-transferring-and-archiving-research-objects
title: BagIt for transferring and archiving Research Objects
categories:
- News
tags:
- Archive
- bagit
- Containers
- Exchange
- Packaging
- RO Bundle
- specification
- ZIP
---
[BagIt](https://tools.ietf.org/html/draft-kunze-bagit-11) is an Internet Draft that specifies a file system structure for transferring and archiving a collection of files, including their checksums and brief metadata. BagIt is commonly used by digital library communities for archival purposes, and is mandated by the Library of Congress for [digital preservation](http://www.digitalpreservation.gov/series/challenge/data-transfer-tools.html).
[Research Object bundles](https://w3id.org/bundle) are structured ZIP-files for serializes a Research Objects, embedding some or all of its resources within the ZIP file, and list the RO content in a manifest, in addition to embedding and referencing annotations and provenance.
While BagIt and RO Bundle might at first seem to provide similar functionalies, the two approaches are complementary in the sense that BagIt focuses on the transfer and consistency checks, recording _checksums_ for resources and their file _sizes_, while RO Bundles focus on the _metadata_, _provenance_ and _annotations_ about the resources, relating them to each other.
[Research Object BagIt archive](https://w3id.org/ro/bagit) defines a profile for a BagIt bag to also be a Research Object. This approach builds on the RO Bundle structure, but modifies it to also be compliant with BagIt.

