# Pinopress

**pinopress** is a modular makefile based static blog generator. that means you run the build script once and every page is generated beforehand.

built in features include markdown generated blog articles, and a rss feed.

## templates

templates are html snippets that you can customize. these templates are then pieced together to form the final html page. **pinopress** makes extensive use of **gnu envsubst** so in each template, you can use variables that will be substituted in on build.

## modules

these have not been implemented yet, but modules are shellscripts that are called during the build process that can add extra features.

here are some potential ideas for modules:
- [ ] syntax highlight for code blocks
- [ ] blog average time to read

## pinopress flavored markdown

pinopress articles are written in an enhanced version of markdown. specification coming soon.

