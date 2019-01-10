Here is a group of links for you to better use Markdown

## Desktop editors 
* __Typora__: a cross-platform desktop tool as both a reader and a writer for Markdown.
	* Link: https://typora.io/
	* Remarks: This is really a nice tool. It would be better if it supports split-panel with both markdown source code and rendered WYSIWYG displayed side-by-side. Also, you have to explicitly turn on the "In-line Math" switch.

* __Boostnote__: An open-source markdown editor for developers on Mac, Windows and Linux. 
	* Link: https://boostnote.io/
	* Github: https://github.com/BoostIO/Boostnote
        - Built with Electron, React + Redux, Webpack, and CSSModules.
* __Gitbook's Editor__: Writing books using git in combination with Markdown or Asciidoc. LaTeX is supported.
	* Download Link for executable binaries (available for Windows / Mac / Linux): https://legacy.gitbook.com/editor
	* Installation instruction for the node.js: https://github.com/GitbookIO/gitbook/blob/master/docs/setup.md
	* Remarks: ~~it has a side-by-side editor, with the left panel showing Markdown source code and the right panel showing WYSIWYG preview.~~ It's official website claims it's equipped with a side-by-side editor but actually I could find it. 

* __ReText__: a cross-platform desktop powerful editor for Markdown and reStructuredText. It is based on [pyqt](https://riverbankcomputing.com/software/pyqt/intro). 
	* Link: https://github.com/retext-project/retext

* __mou__:  a Markdown editor for developers, on Mac OS X. Features live preview, sync scroll, auto save, powerful actions, auto pair, custom themes and CSS, HTML and PDF export, enhanced CJK support and more.
	* Link:http://25.io/mou/

## Online editors
* __Fidus Writer__: an online collaborative editor especially made for academics who need to use citations and/or formulas  that supports citations, collaborative editing, semantic editing and publishing in multiple locations. It's backed by Python.
	* Link: https://github.com/fiduswriter/fiduswriter

* __Dilinger__: a cloud-enabled, mobile-ready, offline-storage, AngularJS powered HTML5 Markdown editor. It does not support Latex syntax yet. It's written in Node.js
	* Link: https://dillinger.io/	

* __马克飞象__: a commercial Evernote extension. But you can still use it as a standalone online editor
	* Link: https://maxiang.io/


## Markdown renderers embeded in a static HTML webpage
With the following  tool, you can just include a single line of JavaScript reference code such as `<script src="...." />`  in your HTML to instantaneously render markdown contents on-the-fly.

* __TeXMe__: a lightweight JavaScript utility to create self-rendering Markdown + LaTeX documents
	* Link: https://github.com/susam/texme
	* To render Markdown-only content without any math content,, use [MdMe](https://github.com/susam/mdme) instead, which is light-weight.

* __markdown page__: Another one-line JS includer for a single static web page with just markdown syntax.
	* Link: https://github.com/oscarmorrison/md-page

* __showdown.js__: Yet another one-line JS includer for a single static web page with just markdown syntax.
	* Link: https://github.com/showdownjs/showdown



## Markdown Extensions  
* __MathJax__: A JavaScript display engine for mathematics that works in all browsers. It's not dedicated to Markdown only, but for generic HTML webpages that needs to render math contents with LaTeX syntax. 
	* Link: https://www.mathjax.org/
	* Source Repo: https://github.com/mathjax/mathjax
	
* __KaTex__: A JavaScript engine for mathematics that is similar to MathJax. But since the render is performed synchronously and doesn’t need to reflow the webpage, the webpage rendering speed is faster than MathJax
	* Link: https://katex.org/
	* Source Repo: https://github.com/KaTeX/KaTeX
	
* __MultiMarkdown__: supports Math, metadata, etc...
	* Link (syntax): https://github.com/fletcher/MultiMarkdown/wiki/MultiMarkdown-Syntax-Guide#footnotes
	* Link: https://github.com/fletcher/MultiMarkdown/

* __markdeep__: an extension of Markdown syntax, plus a static .js file, that supports diagrams, calendars, equations, and other features
    * Link: https://casual-effects.com/markdeep/ 



## Dynamic website generators 
The following tools loads markdown contents and renders them in HTML format
* __Gitbook__: a command line tool (and a Node.js library) for building beautiful books using GitHub/Git and Markdown (or AsciiDoc). It's also equipped with web or desktop editors.
	* Source: https://github.com/GitbookIO/gitbook
	* Samples: https://legacy.gitbook.com/ 

* __Jekyll__: https://jekyllrb.com/
* __Middleman__: https://middlemanapp.com/
* __HamDown__: https://github.com/inem/hamdown
* __Docusaurus__: 
An easy to Maintain Open Source Documentation Websites. It is based on Node.js (React) that converts a directory of Markdown files (along with specified folder structure) to a dynamic, searchable website
	* Link: https://docusaurus.io/ 
	* Github Repo: https://github.com/facebook/Docusaurus
	
## Markdown parsers / SDKs
* __pandoc__: A well-known python structured text parser that supports multiple formats.
	* http://pandoc.org/

* __pymarkup__: This module provides a python wrapper around various text markup languages such as Markdown, reStructuredText and Textile.
	* Link: https://github.com/retext-project/pymarkups

* __kramdown__: a free MIT-licensed Ruby library for parsing and converting a superset of Markdown
	* Link: https://kramdown.gettalong.org/

## Markdown mobile APPs
* __MarkNote__: An open source makrdown note-taking application for Android
	* Source: https://github.com/Shouheng88/MarkNote
	* Download: https://www.coolapk.com/apk/178276
	* Google Play Store: https://play.google.com/store/apps/details?id=me.shouheng.notepal 

## References and Tutorials:
* __commonmark.org__
	* Cheetsheet: https://commonmark.org/help/
	* Interactive Tutorial: https://commonmark.org/help/tutorial/

## Non-markdown
* __[Asciidoctor](https://asciidoctor.org/)__: Asciidoctor is a fast, open source text processor and publishing toolchain for converting AsciiDoc content to HTML5, DocBook, PDF, and other formats. Asciidoctor is written in Ruby and runs on all major operation systems.
