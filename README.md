# Research Object website researchobject.org

This is the GitHub repository for contributing to the [Research Object](http://www.researchobject.org/) website.

The `*.md` files use [MarkDown](https://guides.github.com/features/mastering-markdown) content that is rendered to <https://researchobject.github.io/> by [GitHub pages](https://pages.github.com/). Alias <http://researchobject.org/> will (eventually) map to the same URL space.

Posts in `_posts/` must have a filename like `2019-12-24-.md` and will appear on the bottom of the front page in reverse chronological order.

To add to the top menu, edit `_config.yml`

Note that some subfolders are maintained in [other ResearchObject respositories](https://github.com/ResearchObject):

* [/specifications](https://github.com/ResearchObject/specifications)
* [/ro2019](https://github.com/ResearchObject/ro2019)
* [/ro-crate](https://github.com/ResearchObject/ro-crate)


## Testing locally

To test locally with [Jekyll](https://jekyllrb.com/):

    docker run -it --rm --name jekyll --volume=$(pwd):/srv/jekyll -p 4000:4000 jekyll/jekyll:pages jekyll serve


## Contribute

This repository is coordinated by the [RO-Crate team](https://researchobject.github.io/ro-crate/#contribute).

To suggest changes, improvements or issues, use the GitHub repository
<https://github.com/ResearchObject/ResearchObject.github.io> - if you are new to GitHub or Open
Source you may appreciate the [GitHub guides](https://guides.github.com/) like
[Hello World](https://guides.github.com/activities/hello-world/),
[MarkDown](https://guides.github.com/features/mastering-markdown/) and [How to
contribute to open source](https://opensource.guide/how-to-contribute/)

You are welcome to [join us](https://github.com/ResearchObject/ro-crate/issues/1)! 

Contributors are expected to comply with our [Code of Conduct](CODE_OF_CONDUCT.md)
to ensure an open and inclusive environment.


## License

* © 2010-2020 The University of Manchester, UK

The documentation maintained in this repository is Open Source and licensed as [Apache License, version 2.0](LICENSE), see <https://www.apache.org/licenses/LICENSE-2.0> for details.

Any contributions received are assumed to be [covered by the Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0#contributions).


