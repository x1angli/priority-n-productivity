## Which TeX system to choose?

There are a plethora of [La]Tex systems, such as TeXStudio, Tex Live, MacTeX, CTeX (obsolete), MiKTeX (obsolete).

__TeX Live__  is highly recommended

* [TeX Live](https://www.tug.org/texlive/)
    * Download Links
        * Windows: https://mirrors.tuna.tsinghua.edu.cn/CTAN/systems/texlive/Images/texlive.iso
        * Mac: https://mirrors.tuna.tsinghua.edu.cn/CTAN/systems/mac/mactex/MacTeX.pkg


## What is a TeX editor? 

TeX editors differ from TeX compilers in that tex compilers turns .tex source files into .pdf targets, while TeX editors are usually WYSIWYG frontend UIs. TeX compilers are usually heavy-weight (say, 3GB or 4GB), while TeX editors are sometimes as lightweight as 50MB. 

Sometimes, a TeX system may ship with an out-of-the-box editor plus a compiler. For Tex Live as an instance, it ships with TeXwork as the editor

There are two types of editors: dedicated ones and generic ones.
* Dedicated TeX editors: TeXworks, WinEdt, TeXmaker, XeLaTeX
* Generic editors (with TeX plugins/extensions): VIM, Emacs, VS Code, Sublime, Atom

## Engine and Format?
> Actually, a format is more or less like a document class or a package, except it is associated with a particular command name. Imagine there is a command latex-article that would do the same as latex, except you wouldn't need to say `\documentclass{article}` at the beginning of your file. Similarly, in current distributions, the command pdflatex is the same as the command pdftex except that you don't need to put the instructions to load LATEX at the beginning of your source file. This is convenient, and slightly more efficient too.Formats are great because they implement powerful commands using the basic tools an engine provides. However the power of the format is sometimes limited by the engine's tools set, so people started developing more powerful engines so that other people can implement
even more powerful formats (or packages). 

<sub>Excerpted from http://dante.ctan.org/tex-archive/info/luatex/lualatex-doc/lualatex-doc.pdf</sub>

## Toolkit

#### The combination of __"Texlive + Texmaker"__ 
[Texmaker](http://www.xm1math.net/texmaker/) is a Free cross-platform JIT LaTeX editor. 

#### "TeXStudio + XeLaTeX"
that are shipped in TeXStudio


#### LuaTex (Engine)
http://www.luatex.org/
LuaLATEX is the LuaTEX engine with the LATEX format
an extended version of pdfTeX using Lua as an embedded scripting language. The LuaTeX project's main objective is to provide an open and configurable variant of TeX while at the same time offering downward compatibility. It provides better fonts and font tools

#### FontSpec
https://ctan.org/pkg/fontspec
Fontspec is a package for XELATEX and LuaLATEX.

#### pythontex
The pythontex package allows one to display, execute, and execute & display code in LaTeX. It was originally written for python but now supports quite a few languages.

#### TikZ
TikZ and PGF are TeX packages for creating graphics programmatically. TikZ is build on top of PGF and allows you to create sophisticated graphics in a rather intuitive and easy manner
Note: julia code via pythontex can also generates TikZ.

## What online editors are there?

There are a bunch of online TeX editors/IDEs: OverLeaf, ShareLaTeX 

It's recommended to use online editors to test water before you make a full plunge into your local environment. 

#### codecogs' editor
https://www.codecogs.com/latex/eqneditor.php

## Setting up TUNA

Assuming you are using Tex Live
* Start menu -> Tex Live Manager
* tlmgr option repository, set to `https://mirrors.tuna.tsinghua.edu.cn/CTAN/systems/texlive/tlnet`
* Run the command  `tlmgr install <pkgname>`


## Processing Chinese in TeX

* Use XeLaTeX
* Forget CJK, use UTF-8 or Unicode instead
* Install and use ctex macro package (here, "ctex" is a macro's name, it's not the CTeX compiler.

## Using LaTeX on your website
Here are a list of math typesetting tools for the web
* Katex: https://katex.org/, https://github.com/KaTeX/KaTeX
* MathJax: https://www.mathjax.org/, https://github.com/mathjax/mathjax

### Vim and Latex
#### Taking math notes using Vim and Latex
How I'm able to take notes in mathematics lectures using LaTeX and Vim
https://castel.dev/post/lecture-notes-1/
* The LaTeX plugin in Vim： vimtex
   * https://github.com/lervag/vimtex
   * It is based on LaTeX-Box and it shares a similar goal: to provide a simple and lightweight LaTeX plugin. It provides syntax highlighting, table of contents view, synctex, etc. 
* The plugin config manager: vim-plug
   * https://github.com/junegunn/vim-plug
* utilsnips:
   * UltiSnips is the ultimate solution for snippets in Vim. It has tons of features and is very fast.
   * https://github.com/SirVer/ultisnips

### OCR and Latex
#### MathPix Snip
https://mathpix.com/
This powerful tool would do the magic by recognizing and converting math equation images (either print or handwritten) into formula, all with a single keyboard shortcut. Supports Windows, Mac, and Ubuntu

# References: 
1. [ 《如何使用 LaTeX 排版论文》](https://github.com/tuna/thulib-latex-talk/raw/master/latex-talk.pdf), by 陈晟祺, retreived on Nov 03, 2018. 
1. [How We Wrote a Textbook](http://tim.hibal.org/blog/how-we-wrote-a-textbook/)
1. [上海交通大学 XeLaTeX 学位论文及课程论文模板](https://github.com/sjtug/SJTUThesis)
1. [Matthias Heinkenschloss写的cheatsheet](https://www.caam.rice.edu/~heinken/latex/symbols.pdf)
1. [LaTeX Mathematics' official wiki](https://en.wikibooks.org/wiki/LaTeX/Mathematics)
