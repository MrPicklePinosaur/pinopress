# pinopress

**pinopress** is a modular makefile based static blog generator. that means you run the build script once and every page is generated beforehand.

built in features include markdown generated blog articles, and a rss feed.

## templates

templates are html snippets that you can customize. these templates are then pieced together to form the final html page. edit them to your liking. they can be found in the `templates/` directory. Here's a brief description of each one:

template          | description
------------------|-----------
head              | html before body
foot              | html after body
archivebody       | everything inside body of archive page
archiveitem       | 
rollingbody       | everything inside body of rolling page
rollingitem       |

## modules

these have not been implemented yet, but modules are shellscripts that are called during the build process that can add extra features.

here are some potential ideas for modules:
- [ ] syntax highlight for code blocks
- [ ] blog average time to read

## pinopress flavored markdown

pinopress articles are written in an enhanced version of markdown. specification coming soon.

## variables

 **pinopress** makes extensive use of **gnu envsubst** so in each template, you can use variables that will be substituted in on build. variables can be used in both templates and blog articles. Here's a list of some that you can use:

### global

`$SITEURL` - the SITEURL variable you set in the pinopress config

`$USERGLOBAL1` - global variable you can use however you want

`$USERGLOBAL2` - a second user defined global variable

### article only

`$ARTICLE_TITLE` - title of article, as set in article header

`$PUBLISHED_DATE` - the date/time the article was published, as set in the article header

`$DESCRIPTION` - brief description of the blog post

`$USERLOCAL1` - article specific variable you can use for whatever you want

`$USERLOCAL2` - another user local variable

## mounts

many times, you would like to display a list of html elements somewhere in the page. **pinopress** solves this using mounts. mounts are simply comments that tell pinopress where to append template items.

