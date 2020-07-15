author: stain
date: 2017-07-22 15:56:35+00:00
link: http://www.researchobject.org/2017-07-22-common-workflow-language-viewer/
slug: 2017-07-22-common-workflow-language-viewer
title: 2017-07-22 Common Workflow Language Viewer
categories:
- Presentations
tags:
- cwl
---
On 2017-07-22, Stian Soiland-Reyes [presented](https://www.youtube.com/watch?v=iB_0l-Bm4nA) the [Common Workflow Language Viewer](http://slides.com/soilandreyes/2017-07-22-cwlviewer#/) at [BOSC 2017](https://www.open-bio.org/wiki/BOSC_2017) (ISMB/ECCB), and how it can produce Research Objects to capture [CWL](http://www.commonwl.org/) workflow definitions:

<!-- more -->
One surprise was that our **Common Workflow Language Viewer** poster ([doi:10.7490/f1000research.1114375.1](https://doi.org/10.7490/f1000research.1114375.1)) won a [F1000 Poster Award](https://www.iscb.org/ismbeccb2017/2865#f1000)!
[![ISMB/ECCB 2017 F1000 Poster Award presented to Stian Soiland-Reyes. CWL Viewer: The Common Workflow Language Viewer](http://bioexcel.eu/wp-content/uploads/2017/08/f1000postercertificate-600x408.jpg)](https://www.iscb.org/ismbeccb2017/2865#f1000)
The [poster](https://doi.org/10.7490/f1000research.1114375.1) presents the [CWL Viewer](https://view.commonwl.org/), a web rendering of portable workflow executions defined in the [Common Workflow Language](http://bioexcel.eu/software/workflows/#cwl).
[caption id="attachment_2343" align="alignnone" width="900"][![](http://bioexcel.eu/wp-content/uploads/2017/08/cwlposter-photo.jpg)](http://bioexcel.eu/wp-content/uploads/2017/08/f1000research-167455.pdf) CWL Poster at ISMB/ECCB 2017 - [photo by Michael R Crusoe](https://twitter.com/BioExcelCoE/status/889157731495661570/photo/1). ([doi:10.7490/f1000research.1114375.1](https://doi.org/10.7490/f1000research.1114375.1))[/caption]
The CWL Viewer is already used extensively by the CWL community, it has visualized more than [200 scientific workflows](https://view.commonwl.org/workflows).
At the ISMB/ECCB conference, several talks in the [Bioinformatics Open Source Software](https://www.open-bio.org/wiki/BOSC_2017_Schedule) (BOSC) track related to CWL and reproducibility with scientific workflows.


### Abstract


The [Common Workflow Language](http://www.commonwl.org/) (CWL) project emerged from the BOSC 2014 Codefest as a grassroots, multi-vendor working group to tackle the portability of data analysis workflows. It’s specification for describing workflows and command line tools aims to make them portable and scalable across a variety of computing platforms.
At its heart CWL is a set of structured text files (YAML) with various extensibility points to the format. However, the CWL syntax and multi-file collections are not conducive to workflow browsing, exchange and understanding: for this we need a visualization suite.
[CWL Viewer](https://view.commonwl.org/) is a richly featured CWL visualization suite that graphically presents and lists the details of CWL workflows with their inputs, outputs and steps. It also packages the CWL files into a downloadable Research Object Bundle including attribution, versioning and dependency metadata in the manifest, allowing it to be easily shared. The tool operates over any workflow held in a GitHub repository. Other features include: path visualization from parents and children nodes; nested workflows support; workflow graph download in a range of image formats; a gallery of previously submitted workflows; and support for private git repositories and public GitHub including live updates over versioned workflows.
The CWL Viewer is the de facto CWL visualization suite and has been enthusiastically received by the CWL community.



	
  * Project Website: [https://view.commonwl.org/](https://view.commonwl.org/)

	
  * Source Code: [https://github.com/common-workflow-language/cwlviewer](https://github.com/common-workflow-language/cwlviewer) (doi:[10.5281/zenodo.823535](https://doi.org/10.5281/zenodo.823535))



This blog post is syndicated from [http://bioexcel.eu/poster-award-for-cwlviewer/](http://bioexcel.eu/poster-award-for-cwlviewer/)
Robinson M, Soiland-Reyes S, Crusoe MR and Goble C. (2017): **CWL Viewer: The Common Workflow Language viewer.** _F1000Research _2017, **6**(ISCB Comm J):1075 (poster) (doi: [10.7490/f1000research.1114375.1](https://doi.org/10.7490/f1000research.1114375.1))

