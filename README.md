# Modernisation of MediaFlux Portals functionality

[MediaFlux](http://www.arcitecta.com/Products) includes a Portals
plugin that allows users to create web sites to access their data.

MediaFlux uses [GWT](http://www.gwtproject.org/) to create the
Portal pages.  GWT is a reasonable choice for producing
desktop-application-like web pages, but the HTML generated by
GWT is very resistant to styling via CSS.  CSS is the standard way
of formatting web content.

This project aims at re-imagining Portal output as clean, sensible
HTML.

## Strategy

I've captured the pages generated by MediaFlux for the cat-based
demonstration portal.

### Isolate page components

1. Identified page "components", for example:
  - **Header** is the page header
  - **ListItem** is an item displayed in a list of items
1. Extracted HTML for each "component" into separate files
1. Replaced each component with a reference to the file containing
   the extracted HTML for that component
1. Written a shell script to re-assemble the page by starting with
   the main page and replacing file references with the HTML from
   that component file
1. Verifying the assembled page looks like the original

This produces a set of files that each represent a page component.

### Replace components with clean versions

With each component file, I replaced the millions-of-nested-tables
HTML generated by GWT with clean, simple HTML.  The functionality
of the page is verified by re-assembling the page out of components.

## Repo Structure

(work in progress)
