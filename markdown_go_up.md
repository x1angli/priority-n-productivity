Here is a group of links for you to better use Markdown

## Desktop  editors 
* __Typora__: a cross-platform desktop tool as both a reader and a writer for Markdown.
	* Link: https://typora.io/
	* Remarks: This is really a nice tool. It would be better if it supports split-panel with both markdown source code and rendered WYSIWYG displayed side-by-side. Also, you have to explicitly turn on the "In-line Math" switch.

* __Gitbook's Editor__: Writing books using git in combination with Markdown or Asciidoc. LaTeX is supported.
	* Download Link for executable binaries (available for Windows / Mac / Linux): https://legacy.gitbook.com/editor
	* Installation instruction for the node.js: https://github.com/GitbookIO/gitbook/blob/master/docs/setup.md
	* Remarks: ~~it has a side-by-side editor, with the left panel showing Markdown source code and the right panel showing WYSIWYG preview.~~ It's official website claims it's equipped with a side-by-side editor but actually I could find it. 

* __ReText__: a cross-platform desktop powerful editor for Markdown and reStructuredText. It is based on [pyqt](https://riverbankcomputing.com/software/pyqt/intro). 
	* Link: https://github.com/retext-project/retext

## Online editors
* __Fidus Writer__: an online collaborative editor especially made for academics who need to use citations and/or formulas  that supports citations, collaborative editing, semantic editing and publishing in multiple locations. It's backed by Python.
	* Link: https://github.com/fiduswriter/fiduswriter

## Markdown renderers embeded in a static HTML webpage
With the following  tool, you can just include a single line of JavaScript reference code such as `<script src="...." />`  in your HTML to instantaneously render markdown contents on-the-fly.

* __TeXMe__: a lightweight JavaScript utility to create self-rendering Markdown + LaTeX documents
	* Link: https://github.com/susam/texme
	* To render Markdown-only content without any math content,, use [MdMe](https://github.com/susam/mdme) instead, which is light-weight.

* __markdown page__: Another one-line JS includer for a single static web page with just markdown syntax.
	* Link: https://github.com/oscarmorrison/md-page


##   Markdown Extensions  
* __MathJax__: A JavaScript display engine for mathematics that works in all browsers. It's not dedicated to Markdown only, but for generic HTML webpages that needs to render math contents with LaTeX syntax. 
	* Link: https://www.mathjax.org/

* __markdeep__: an extension of Markdown syntax, plus a static .js file, that supports diagrams, calendars, equations, and other features
    * Link: https://casual-effects.com/markdeep/ 


## Markdown parsers / SDKs
* __pandoc__: A well-known python structured text parser that supports multiple formats.
	* http://pandoc.org/

* __pymarkup__: This module provides a python wrapper around various text markup languages such as Markdown, reStructuredText and Textile.
	* Link: https://github.com/retext-project/pymarkups

* __kramdown__: a free MIT-licensed Ruby library for parsing and converting a superset of Markdown
	* Link: https://kramdown.gettalong.org/

## Dynamic website generators 
The following tools loads markdown contents and renders them in HTML format
* __Gitbook__: a command line tool (and a Node.js library) for building beautiful books using GitHub/Git and Markdown (or AsciiDoc). It's also equipped with web or desktop editors.
	* Source: https://github.com/GitbookIO/gitbook
	* Samples: https://legacy.gitbook.com/ 

* __Jekyll__: https://jekyllrb.com/
* __Middleman__: https://middlemanapp.com/
* __HamDown__: https://github.com/inem/hamdown
