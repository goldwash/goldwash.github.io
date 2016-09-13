# site
Staging area for site as of early September 2016. By Lukas (http://ltwp.net)

# How To Update Your Site (goldwashmusic.com)

## What’s Going On

Github.com is hosting all of your files; that is, they have servers that are keeping all of the code powering your site and when someone goes to goldwashmusic.com, github delivers the files to load the page in their browser. Github generously does this for free via [Github pages](https://pages.github.com/)!

You own a domain name through **Squarespace**, and this costs a yearly fee. We have associated that domain name to github, so that the URL goldwashmusic.com prompts github to present the documents. 

The site is generated by a “Static Site Generator” called [Jekyll](http://jekyllrb.com/). This is a form of “Content Management System” (CMS)—which helps us keep track of all the info on the site, and so if we edit something in once place—for instance, the footer material, all footers on the entire site update. 

Github and Jekyll play nice together. If we were using Jekyll without github, we would ask Jekyll to “build” the site, and then upload that “compiled” site to a server somewhere. Github _automatically_ builds the site, so we don’t have to! And it makes it easily updatable. 

## How is Jekyll Organized?

I’ve stripped Jekyll down to just what we need—“content” and “templates”. In the “repository”/directory of your site, you should see this list of things, or something close to it:

![jekyll repo structure](howto1.png)

Basically, `_config.yml` has some abstract-level variables for the site. `_includes` has some snippets of HTML that appear on multiple pages (so editing these edits them everywhere). `_site` is where Jekyll builds the site—we can ignore this thanks to github!

The `_layouts` directory is particularly important; this has the HTML templates. There are only two for Goldwash, a splash/“index” page, and “column”—which is the layout for the home page and shows page. If we want to seriously overhaul the site, this is where to make changes. Otherwise, we can just edit “content” files. 

## How do I edit the page contents?

In general, the HTML files in the top-level directory—`home.html`, `index.html`, and `shows.html` can be edited to quickly change the content. You’ll see these files have some stuff at the top, which tells Jekyll which layout to use. 

e.g. we want the `/home.html` page to use the “column.html” layout, and we want the top button to say “SHOWS”. And we want this home page to have some soundcloud embeds and divider bars, so `home.html` looks like this: 

![sample page](howto2.png)

If you want to swap what’s embedded, or change what’s on the shows page, open up their respective HTML files and make the changes under the triple hyphens (`---`) of top matter. 

When you make these changes, I assume you’ll be doing so _locally_, or on your own computer. Once you’ve done so, you’ll want to “sync” up with the web version on github so that those changes appear online. This is most easily done via the [github app](https://desktop.github.com/) unless you want to do it via command line, which is cool too. 

## Need to change more than just content?

Talk to me! Jekyll should be pretty intuitive to anyone who has worked with a static-site generator before, too. 

Jekyll and Github Pages both have great documentation for their services. 

I’ll amend this document as need-be, if you have any issues!

11 Sept 2016 - Lukas WP / lukas@ltwp.net