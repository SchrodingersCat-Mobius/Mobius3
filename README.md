# Möbius3

Repository for all my things Möbius.

This repository is used to manage a Github-Pages site located at <https://schrodingerscat-mobius.github.io/Mobius3/>

The website is contained within the `docs` folder which is built using [Quarto](https://quarto.org/).

Quarto is free open-source software available for Windows, MacOS and Linux and may be downloaded from<https://quarto.org/docs/get-started/>.

Information on creating and customising websites using Quarto can be found at:
* Creation:  <https://quarto.org/docs/websites/>
* Website Navigation: <https://quarto.org/docs/websites/website-navigation.html>
* Publishing to Github Pages: <https://quarto.org/docs/publishing/github-pages.html>

## My workflow used to create the website

1. Using GitHub Desktop, create the new empty repository `Mobius3` and publish this to GitHub as a public repo.
2. Open a bash shell or windows command shell in the root of the local clone of the repo and create a skeleton website using `quarto create project website ../Mobius3`.
3. Open `_quarto.yml` in `Notepad++` and configure the website settings as desired.
    i. Add `output-dir: docs` immediately below `type: website`
	ii. Add `favicon` entry immediately above `title` entry
	iii. Change title of website to `Schrödinger's Cat's Möbius 3 Site`
	iv. Modify `navbar` entry to remove links in site's title header and add icon
	v. Add `sidebar` entry to create left hand side navigation menu
	vi. Add nested `contents:` and `section:` entries to control structure of website and what directories and sub-directories are used for building content. (Could also use `auto: *.qmd` for less hands-on approach which will use all directories and sub-directories containing Quarto markdown files to build the content and the directory heirarchy to determine the structure.)
	vii. Add `page-navigation: true` to add navigation arrows at bottom of each webpage.
	viii. Modify html format by replacing `cosmo` theme with `light` theme of `sandstone` and `dark` theme of `cyborg`
	ix. Add `toc-expand` and `toc-depth` entries to control aspects of appearance of left hand side menu.
4. Add a `.nojekyll` file to the root of the repo so that GitHub will not do any additional processing when we publish the website. Use `touch .nojekyll` from bash shell or `copy NUL .nojekyll` from windows command shell.
5.  Organise content by creating directories and subdirectories containing Quarto markdown files `.qmd` hierarchy in the local repo. Place any images (or videos) embedded in a page in an `images` folder at the same level as the `qmd` file as good housekeeping.
6. While editing, create a live preview of the website by entering `quarto preview` in a bash shell or windows command shell opened in the root of the repo.
7. When editing is complete, render the entire website by using `quarto render` in the bash shell or command window.
8. Commit changes and push to GitHub using GitHub Desktop.
9. (This step is only necessary once.) In the repo on GitHub go to `Settings`, select `Pages` under `Code and Automation`. Under `Build and Deployment`, set Source to `Deploy from a branch`. Under `Branch`, choose `main` and `/docs` and then click on `Save`.
10. The URL for the GitHub Pages site is of the form `http://<username>.github.io/<repository>` which for this site is <https://schrodingerscat-mobius.github.io/Mobius3/>.

