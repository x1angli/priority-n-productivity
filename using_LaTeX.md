## Which TeX engine to choose?

There are a plethora of [La]Tex engines, such as Tex Live, CTeX, MiKTeX, MacTeX. Here the term "editor" may essentially mean a full spectrum ranging from lightweight text-like editors to fully-fledged IDEs.

### We recommend the following ones: 
1. [TeX Live](https://www.tug.org/texlive/), download from [the TUNA mirror](https://mirrors.tuna.tsinghua.edu.cn/CTAN/systems/texlive/Images/texlive.iso), [MAC dmg file](https://mirrors.tuna.tsinghua.edu.cn/
CTAN/systems/mac/mactex/MacTeX.pkg). 

## Which TeX editor to choose? 
* Dedicated TeX editors: TeXStudio, TeXworks, WinEdt, TeXmaker, XeLaTeX
* Generic editors (with TeX plugins/extensions): VIM, Emacs, VS Code, Sublime, Atom
* Online editors/IDEs: OverLeaf, ShareLaTeX 

### We recommend the following ones: 
1. [Texmaker](http://www.xm1math.net/texmaker/), a Free cross-platform JIT LaTeX editor. 

## Whats the difference between a TeX engine and a TeX editor?
TeX engines are engines plus packages. TeX editor is merely a WYSIWYG (probably) UI. So, merely installing a TeX editor is far from enough -- you have to install a TeX engine/compiler. Personally, I use Texlive + Texmaker

## Setting up TUNA

Assuming you are using Tex Live
* Start menu -> Tex Live Manager
* tlmgr option repository, set to `https://mirrors.tuna.tsinghua.edu.cn/CTAN/systems/texlive/tlnet`
* Run the command  `tlmgr install <pkgname>`


## Processing Chinese in TeX
* Use XeLaTeX
* Forget CJK, use UTF-8 or Unicode instead
* Install and use ctex macro package (here, "ctex" is a macro's name, it's not the CTeX compiler.

# References: 
1. [ 《如何使用 LaTeX 排版论文》](https://github.com/tuna/thulib-latex-talk/raw/master/latex-talk.pdf), by 陈晟祺, retreived on Nov 03, 2018. 
