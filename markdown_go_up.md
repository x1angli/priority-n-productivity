Here is a group of links for you to better use Markdown

## Desktop editors 

#### Typora
 * a cross-platform desktop tool as both a reader and a writer for Markdown.
 * Link: https://typora.io/
 * Remarks: This is really a nice tool. It would be better if it supports split-panel with both markdown source code and rendered WYSIWYG displayed side-by-side. Also, you have to explicitly turn on the "In-line Math" switch.

#### Boostnote
 * An open-source markdown editor for developers on Mac, Windows and Linux. 
 * Link: https://boostnote.io/
 * Github: https://github.com/BoostIO/Boostnote
        - Built with Electron, React + Redux, Webpack, and CSSModules.

#### Notable
 * An Electron-based markdown note-taking app. the app isn't bloated, the app has a pretty interface, tags are indefinitely nestable and can import Evernote note
 * Github: https://github.com/fabiospampinato/notable
        
#### Gitbook's Editor
 * Writing books using git in combination with Markdown or Asciidoc. LaTeX is supported.
 * Download Link for executable binaries (available for Windows / Mac / Linux): https://legacy.gitbook.com/editor
 * Installation instruction for the node.js: https://github.com/GitbookIO/gitbook/blob/master/docs/setup.md
 * Remarks: ~~it has a side-by-side editor, with the left panel showing Markdown source code and the right panel showing WYSIWYG preview.~~ It's official website claims it's equipped with a side-by-side editor but actually I could find it. 

#### Hve Notes
* It's both a desktop Markdown editor and Github publisher
* Link: https://hvenotes.fehey.com/
* Github: https://github.com/hve-notes/hve-notes

#### ReText
 * a cross-platform desktop powerful editor for Markdown and reStructuredText. It is based on [pyqt](https://riverbankcomputing.com/software/pyqt/intro). 
 * Link: https://github.com/retext-project/retext

#### mou
 * a Markdown editor for developers, on Mac OS X. Features live preview, sync scroll, auto save, powerful actions, auto pair, custom themes and CSS, HTML and PDF export, enhanced CJK support and more.
 * Link: http://25.io/mou/

## Text editor plugins / extensions
### VSCode plugins

#### Markdown All in One
 * Link: https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one
 
#### Markdown+Math
 * Link: https://marketplace.visualstudio.com/items?itemName=goessner.mdmath

#### Markdown Support for Visual Studio Code
 * Provide features like: keyboard shortcuts (toggle bold, italic, code span, strikethrough and heading), list editing, TOC, Print Markdown to HTML, Math
 
#### Markdown Preview Github Styling
 * Changes VS Code's built-in markdown preview to match Github's styling
 * Link: https://marketplace.visualstudio.com/items?itemName=bierner.markdown-preview-github-styles


## Online editors
#### Md2All （推荐）
Markdown排版利器，支持 "一键排版" 、自定义css、80多种代码高亮。能让Markdown内容，无需作任何调整就能一键复制到微信公众号、博客园、掘金、知乎、csdn、51cto、WordPress、hexo……等平台，并且保留源代码高亮的样式。支持把图片自动上传到云图床。支持Latex数学公式在公众号等平台完美显示。
 * 介绍：https://www.cnblogs.com/garyyan/p/8329343.html
 * 在线版: http://md.aclickall.com/

#### 微信公众号排版编辑器
 * 介绍：https://mp.weixin.qq.com/s/pn0LzyfgUj6rGUfVHUksjg
 * 在线版: https://lab.lyric.im/wxformat/
 * Github repo: https://github.com/lyricat/wechat-format


#### Fidus Writer
 * an online collaborative editor especially made for academics who need to use citations and/or formulas  that supports citations, collaborative editing, semantic editing and publishing in multiple locations. It's backed by Python.
 * This extension only styles the markdown preview. Use this extension pack to add support for other Github-specific markdown features
 * Link: https://github.com/fiduswriter/fiduswriter

#### Dilinger
 * a cloud-enabled, mobile-ready, offline-storage, AngularJS powered HTML5 Markdown editor. It does not support Latex syntax yet. It's written in Node.js
 * Link: https://dillinger.io/    

#### 马克飞象
 * a commercial Evernote extension. But you can still use it as a standalone online editor
 * Link: https://maxiang.io/

 
## Markdown renderers embeded in a static HTML webpage
 * With the following  tool, you can just include a single line of JavaScript reference code such as `<script src="...." />`  in your HTML to instantaneously render markdown contents on-the-fly.

#### TeXMe
 * a lightweight JavaScript utility to create self-rendering Markdown + LaTeX documents
 * Link: https://github.com/susam/texme
 * To render Markdown-only content without any math content,, use [MdMe](https://github.com/susam/mdme) instead, which is light-weight.

#### markdown page
 * Another one-line JS includer for a single static web page with just markdown syntax.
 * Link: https://github.com/oscarmorrison/md-page

#### showdown.js
 * Yet another one-line JS includer for a single static web page with just markdown syntax.
 * Link: https://github.com/showdownjs/showdown



## Markdown Extensions 

### MathJax

#### MathJax
 * A JavaScript display engine for mathematics that works in all browsers. It's not dedicated to Markdown only, but for generic HTML webpages that needs to render math contents with LaTeX syntax. 
 * Link: https://www.mathjax.org/
 * Source Repo: https://github.com/mathjax/mathjax

#### TeX All the Things
An extension which lets you enable LaTeX on any website (including Github). Typesets any LaTeX found on webpages using MathJax (http://www.mathjax.org/).

#### KaTex
 * A JavaScript engine for mathematics that is similar to MathJax. But since the render is performed synchronously and doesn’t need to reflow the webpage, the webpage rendering speed is faster than MathJax
 * Link: https://katex.org/
 * Source Repo: https://github.com/KaTeX/KaTeX
    
#### MultiMarkdown
 * supports Math, metadata, etc...
 * Link (syntax): https://github.com/fletcher/MultiMarkdown/wiki/MultiMarkdown-Syntax-Guide#footnotes
 * Link: https://github.com/fletcher/MultiMarkdown/

#### markdeep
 * an extension of Markdown syntax, plus a static .js file, that supports diagrams, calendars, equations, and other features
 * Link: https://casual-effects.com/markdeep/ 



## Dynamic website generators
The following tools loads markdown contents and renders them in HTML format

#### Gitbook
 * a command line tool (and a Node.js library) for building beautiful books using GitHub/Git and Markdown (or AsciiDoc). It's also equipped with web or desktop editors.
 * Source: https://github.com/GitbookIO/gitbook
 * Samples: https://legacy.gitbook.com/ 

#### Jekyll
 * https://jekyllrb.com/

#### Middleman
 * https://middlemanapp.com/

#### HamDown
 * https://github.com/inem/hamdown
 
#### Docusaurus
 * An easy to Maintain Open Source Documentation Websites. It is based on Node.js (React) that converts a directory of Markdown files (along with specified folder structure) to a dynamic, searchable website
 * Link: https://docusaurus.io/ 
 * Github Repo: https://github.com/facebook/Docusaurus
 
#### Hve Notes
* It's both a desktop Markdown editor and Github publisher
* Link: https://hvenotes.fehey.com/
* Sample: https://fehey.com/


## Markdown parsers / converters / SDKs

#### pandoc
 * A well-known python structured text parser that supports multiple formats.
 * http://pandoc.org/
    * Tips: [Customizing pandoc to generate beautiful pdfs from markdown](https://learnbyexample.github.io/tutorial/ebook-generation/customizing-pandoc/) 
#### pymarkup
 * This module provides a python wrapper around various text markup languages such as Markdown, reStructuredText and Textile.
 * Link: https://github.com/retext-project/pymarkups

#### kramdown
 * a free MIT-licensed Ruby library for parsing and converting a superset of Markdown
 * Link: https://kramdown.gettalong.org/

### Python parsers

#### mistletoe
 * A fast, extensible and spec-compliant Markdown parser in pure Python.
 * https://github.com/miyuchina/mistletoe

#### mistune
 * The fastest markdown parser in pure Python with renderer feature. 
 * http://mistune.readthedocs.io/
 * https://github.com/lepture/mistune

### Markdown pitch deck (slides) generator 
#### markdeck
 * It converts a markdown to a clean, local-hosted, html5 slide deck (PPT-style presentation deck). It takes \*.md files in markdown format and the assets subdir and renders a html5 slidedeck, using pandoc as converter and reveal.js as the presenter framework. It's based on markdown, pandoc, reveal.js, plantuml, ditaamini, asciitosvg, graphviz, asciinema, decktape, vega-lite, mathjax-pandoc-filter, and font-awesome.
 * Link: https://arnehilmann.github.io/markdeck/
 * Github Repo: https://github.com/arnehilmann/markdeck
    
#### nodeppt
 * It converts a markdown to a clean, local-hosted, html5 slide deck (PPT-style presentation deck). It's based on webslides、webpack、markdown-it、posthtml
 * Link: http://js8.in/nodeppt
 * Github Repo: https://github.com/ksky521/nodeppt 
 
#### marp
* https://yhatt.github.io/marp/

### Markdown resume (curriculum vitae) generator

#### 冷熊简历（中文）
* Link: http://cv.ftqq.com/#

## Markdown mobile APPs

#### MarkNote
 * An open source makrdown note-taking application for Android
 * Source: https://github.com/Shouheng88/MarkNote
 * Download: https://www.coolapk.com/apk/178276
 * Google Play Store: https://play.google.com/store/apps/details?id=me.shouheng.notepal 


## References and Tutorials

#### commonmark.org
 * Cheetsheet: https://commonmark.org/help/
 * Interactive Tutorial: https://commonmark.org/help/tutorial/

## Non-markdown
#### Asciidoctor
 * https://asciidoctor.org/
 * Asciidoctor is a fast, open source text processor and publishing toolchain for converting AsciiDoc content to HTML5, DocBook, PDF, and other formats. Asciidoctor is written in Ruby and runs on all major operation systems.
