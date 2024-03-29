
# My personal notes

### For Mac OS installation and running

See below the appropriate, updated section.

### Updating publications design

I'm not so happy with the design, I find it a bit tricky to update, as the script provided in `markdown_generator` relies on a TSV file, and cannot be automatically updated from a bibTex file. 
I'd rather modify it. I've now created a `scripts` folder based on the one created by Nelle for our compbio website. 

- It is now possible to automatically generate md files from a bibtex file, within the dedicated folder `biblio`
- Now, the file `_includes/archive-single.html` needs to be updated, or modified in order to 
    - directly feed on generated md files
    - display in a way I like (i.e. remove verbous forms...)
- Also, Nelle's script to generate md files from bib file should be modified to add fields... See which fields: e.g., journal, date, etc...

=> make a combination between the `_includes/archive-single.html` files from this repo and our compbio website?

TO DO that:

- [x] Create a fixed file based on `_includes/archive-single.html` => `_includes/archive-single-bib.html`
- [x] Include it in `_pages/publications.md`
- [x] Fix link to Googlescholar... in `_pages/publications.md` => was not working cause ref to author. 
- [ ] Fix format of refs in new file
- [x] Check why the three example pubs are still used... cause kept in examples folder? YES! Moved to Trash

### Publishing the site

Use of Gh-Pages. Deployed, but for now does not work (as of **7th of Mar 2023**).

Have a look here? https://josephtingiris.github.io/jekyll/github/metadata/2017/10/15/no-github-api-authentication-could-be-found/ 
Otherwise, ask Nelle...

### Site design

- [x] Remove for now unused sections: Talks, Teaching?
- [x] Remove same sections from CV page
- [x] Use CV publications' design on the publications page: modif file `_pages/publications.md` to include same file as file `_pages/cv.md`: `archive-single-cv.html` instead of `archive-single-bib.html`


# Notes provided with Academic pages
A Github Pages template for academic websites. This was forked (then detached) by [Stuart Geiger](https://github.com/staeiou) from the [Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/), which is © 2016 Michael Rose and released under the MIT License. See LICENSE.md.

I think I've got things running smoothly and fixed some major bugs, but feel free to file issues or make pull requests if you want to improve the generic template / theme.

### Note: if you are using this repo and now get a notification about a security vulnerability, delete the Gemfile.lock file. 

# Instructions

1. Register a GitHub account if you don't have one and confirm your e-mail (required!)
1. Fork [this repository](https://github.com/academicpages/academicpages.github.io) by clicking the "fork" button in the top right. 
1. Go to the repository's settings (rightmost item in the tabs that start with "Code", should be below "Unwatch"). Rename the repository "[your GitHub username].github.io", which will also be your website's URL.
1. Set site-wide configuration and create content & metadata (see below -- also see [this set of diffs](http://archive.is/3TPas) showing what files were changed to set up [an example site](https://getorg-testacct.github.io) for a user with the username "getorg-testacct")
1. Upload any files (like PDFs, .zip files, etc.) to the files/ directory. They will appear at https://[your GitHub username].github.io/files/example.pdf.  
1. Check status by going to the repository settings, in the "GitHub pages" section
1. (Optional) Use the Jupyter notebooks or python scripts in the `markdown_generator` folder to generate markdown files for publications and talks from a TSV file.

See more info at https://academicpages.github.io/

## To run locally (not on GitHub Pages, to serve on your own computer)

1. Clone the repository and made updates as detailed above
1. Make sure you have ruby-dev, bundler, and nodejs installed: `sudo apt install ruby-dev ruby-bundler nodejs`
1. Run `bundle clean` to clean up the directory (no need to run `--force`)
1. Run `bundle install` to install ruby dependencies. If you get errors, delete Gemfile.lock and try again.
1. Run `bundle exec jekyll liveserve` to generate the HTML and serve it from `localhost:4000` the local server will automatically rebuild and refresh the pages on change.

## Instructions to run locally on Mac OS

We'll be using a virtual environment. See also this page: <https://hackmd.io/@AstrobioMike/jekyll-conda-setup>.

    conda create -y -n jekyllenv -c conda-forge rb-jekyll c-compiler compilers cxx-compiler python
    conda activate jekyllenv
    #gem install bundler:2.3.14
    gem install bundler

Then:
    bundle clean
    bundle update
    bundle exec jekyll serve

On the next occurrences:
    jekyll serve

NB: 
1. Run `bundle clean` to clean up the directory (no need to run `--force`)
1. Run `bundle install` to install ruby dependencies. If you get errors, delete Gemfile.lock and try again.
1. Run `bundle exec jekyll serve` to generate the HTML and serve it from `localhost:4000` the local server will automatically rebuild and refresh the pages on change.

# Changelog -- bugfixes and enhancements

There is one logistical issue with a ready-to-fork template theme like academic pages that makes it a little tricky to get bug fixes and updates to the core theme. If you fork this repository, customize it, then pull again, you'll probably get merge conflicts. If you want to save your various .yml configuration files and markdown files, you can delete the repository and fork it again. Or you can manually patch. 

To support this, all changes to the underlying code appear as a closed issue with the tag 'code change' -- get the list [here](https://github.com/academicpages/academicpages.github.io/issues?q=is%3Aclosed%20is%3Aissue%20label%3A%22code%20change%22%20). Each issue thread includes a comment linking to the single commit or a diff across multiple commits, so those with forked repositories can easily identify what they need to patch.
