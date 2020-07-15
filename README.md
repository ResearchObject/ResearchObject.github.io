GitHub Pages source for <http://researchobject.org/>

To test locally:

    docker run -it --rm --name jekyll --volume=$(pwd):/srv/jekyll -p 4000:4000 jekyll/jekyll:pages jekyll serve
