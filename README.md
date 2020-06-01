# Wiki

**Source code for [spacehuhn.wiki](https://spacehuhn.wiki)**  

![github pages](https://github.com/SpacehuhnTech/wiki/workflows/github%20pages/badge.svg)  

## How to contribute

1. [Install Hugo](https://gohugo.io/getting-started/installing)
2. `git clone https://github.com/SpacehuhnTech/wiki.git` or [Download ZIP](https://github.com/SpacehuhnTech/wiki/archive/master.zip)
3. Run `hugo server -D` inside the repository folder
4. Open [localhost:1313](http://localhost:1313/) to see a live render of the Wiki
5. Work on the site
6. If you're done editing, commit your changes and [create a pull request](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request)

**Do not edit the [gh-pages branch](https://github.com/SpacehuhnTech/wiki/tree/gh-pages).**  
A push on the master branch will trigger a Github action to automatically generate the static files and place them on the gh-pages branch.  

* Edit existing pages in `content/en/`
* Create a page using `hugo new YOUR_FILE_PATH.md`
* Create a new chapter using `hugo new YOUR_FILE_PATH.md --kind chapter`
* Images are placed in `static/media/`
  
## Credits

Inspired by [pwnagotchi.ai](https://pwnagotchi.ai/).  
Build with [Hugo](https://gohugo.io/) and [Hugo Learn Theme](https://github.com/matcornic/hugo-theme-learn/).

## License

This software is licensed under the MIT License. See the [license file](LICENSE) for details.  
