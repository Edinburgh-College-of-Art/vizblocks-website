# Read Me

Hello!

Welcome behind the curtain of the VizBlocks website.

The code can look a bit intimidating, but once you have your bearings it is quite intuitive.

## Running Jekyll

First you will need to install *Jekyll* onto your machine. This can be done by following step 1 and 2 of the [quickstart tutorial on the Jekyll website](https://jekyllrb.com/docs/).

Then, navigate in the terminal to the folder holding the VizBlocks website. A useful cheat here can be to type `cd ` into the terminal, drag and drop the folder into the terminal window and then press enter.

Once in ../vizblocks-website/ run `bundle install`, then `bundle exec jekyll serve`. This will spin up a development server at [localhost:4000].

Now, any changes you make to the website will be pushed to the server when you save the page. You just need to refresh the browser window to see them.

## Updating Content

The content for the site is organised in collection folders.

Folder        | Info
--------------|--------------
`/_authors`   |Information about people who have worked on the project.
`/_blocks`    |Information about the types of blocks we have built so far.
`/_builds`    |Information about projects have have used the VizBlocks framework.
`/_data`      |Miscellaneous information including home page content, contact info, navigation links, funding info.
`/_tutorials` |Tutorials, which can be written as markdown documents.

New authors, blocks, builds and tutorials can be added by duplicating an existing file, and replacing the old content. The duplication is helpful to keep the format of the front matter data correct.

After checking that the new content looks nice on the page, you can push the changes to the git repo, which will automatically be mirrored to the live site.

## Some jobs to be done:

- Studio photographs of the blocks
- Studio videos of the behaviours
- Turn behaviour videos into .gifs
- Fill in home page content
- Write tutorials
- Mirror documentation from VizBlocks Framework repo
- Node-RED demo applet
- Block Visualiser applet
- VizBlocks Node-RED node

## Important!

- Currently the links in the documentation header are hard coded to point to the github page - if we later want to host the site elsewhere, these will have to be changed.
