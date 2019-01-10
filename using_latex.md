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

## Recommended systems / combinations

1. The combination of __"Texlive + Texmaker"__ 
[Texmaker](http://www.xm1math.net/texmaker/) is a Free cross-platform JIT LaTeX editor. 

1. "TeXStudio + XeLaTeX" that are shipped in TeXStudio

## What online editors are there?

There are a bunch of online TeX editors/IDEs: OverLeaf, ShareLaTeX 

It's recommended to use online editors to test water before you make a full plunge into your local environment. 


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

# References: 
1. [ 《如何使用 LaTeX 排版论文》](https://github.com/tuna/thulib-latex-talk/raw/master/latex-talk.pdf), by 陈晟祺, retreived on Nov 03, 2018. 
