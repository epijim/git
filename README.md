Using git cheatsheet
======================

## Wait, where is everything?

See **how this works** below. To see the rendered version of this repo, go to https://pages.github.roche.com/RWDS-sme/IPSOS/. 

## How this works

This repo contains markdown files (*end in* `.md`). The text of the site actually comes from the markdown files in the posts folder. The footer, header, and styling come from the `_includes` folder, and the `.js`, `.html` and `.css` files.

The magic comes from the file called `_config.yml`, and the fact the branch in github is called `gh-pages`. Github knows that when it sees this branch, it needs to server the repo publically as a website, and it also knows that when it sees that `.yml` file - the site is still in markdown and needs to be processed into `.html` first.

Github is using an engine called *jekyll* to process the markdown into `.html`. R does the same thing - although it first converts Rmarkdown to markdown (and runs the scripts), then *jekyll* takes it from markdown to `.html`.

## Contributing

Wanna update this? From github, either [open an issue](https://github.roche.com/RWDS-sme/IPSOS/issues/new) to ask to make a change... or, get in the code and edit yourself using the steps below.

### Little changes

1. Use the editor on github to make changes, then when committing, click "create a new branch for this commit and start a pull request".
2. Your changes will be wrapped up, and a repo owner can then rubber stamp them before they are deployed to the site

### Bigger changes

Multiple ways to do this - e.g. you could make the branch in github or locally, so below is just one method.

1. `git clone` the repo locally
2. `git branch` then `checkout` your new branch, which has a simple but useful name.
3. Make your edits and commit them.
4. Push your branch up, then make a pull request to have your changes merged in.
5. A repo owner can then rubberstamp them.
