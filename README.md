# Wiki

**Source code for [spacehuhn.wiki](https://spacehuhn.wiki)**  

![github pages](https://github.com/SpacehuhnTech/wiki/workflows/github%20pages/badge.svg)  

## How to contribute

1. [Install Hugo](https://gohugo.io/getting-started/installing)
2. Run `git clone https://github.com/SpacehuhnTech/wiki.git` 
3. Open the repo `cd wiki` and download the learn theme by running `git submodule update --init --recursive`
4. Run `hugo server -D` inside the repository folder
5. Open [localhost:1313](http://localhost:1313/) to see a live render of the Wiki
6. Work on the site
7. If you're done editing, commit your changes and [create a pull request](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request)

## How to create/edit pages

* Edit existing pages in `content/en/`
* Images are placed in `static/media/`
* Create a page by running `hugo new YOUR_FILE_PATH.md` from the `wiki/` folder
* Create a new chapter by running `hugo new YOUR_FILE_PATH.md --kind chapter` from the `wiki/` folder

**Some useful links:**  
* [Markdown](https://learn.netlify.app/en/cont/markdown/)
* [Hugo Shortcodes](https://gohugo.io/content-management/shortcodes/)
* [Hugo Learn Theme Shortcodes](https://learn.netlify.app/en/shortcodes/)
* [Hugo Documentation](https://gohugo.io/documentation/)
* [Hugo Learn Theme Documentation](https://learn.netlify.app/en/)

## Credits

Inspired by [pwnagotchi.ai](https://pwnagotchi.ai/).  
Build with [Hugo](https://gohugo.io/) and [Hugo Learn Theme](https://github.com/matcornic/hugo-theme-learn/).

## License

This software is licensed under the MIT License. See the [license file](LICENSE) for details.  
