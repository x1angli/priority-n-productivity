This is intended for newbies to setup an environment for data scientists and engineers located in mainland China.

### 目标 / Motivation: ###
Anaconda 是一个用于科学计算的“全家桶”，支持 Linux, Mac, Windows, 包含了Python，包含了Jupyter Notebook，更集成了众多流行的科学计算、数据分析的包。

由于国际出口带宽的瓶颈限制，下载和使用Anaconda是一件苦差事。安装文件本身就达到600MB，第三方包会更大。如果不用本文中提到的方法加速，一方面用户的等待时间会很长，另一方面一旦出错就会前功尽弃，导致用户或初学者很有挫折感。本指南就是通过TUNA的镜像来解决上述问题，从而提升用户体验和生产力。

By [its website](https://www.anaconda.com/),  "Anaconda is The Most Popular Python Data Science Platform". 

Due to poor internet connection in certain regions, using integrated tools such as Anaconda is always painful, especially consider the hefty size of 600MB for its installer (much less to say about 3rd-party packages/modules). Most users might be frustrated. This instruction is written to solve this issue. The main idea behind the following approach: use a mirror site to accelerate the download process to enhance user experience and boost productivity.

## TL'DR 简短版 ##
 
如果你只是一个轻度的学习者，想在有限的时间内大致接触一下，我建议用在线版的 Google Colab
* https://colab.research.google.com
* https://colab.research.google.com/notebooks/welcome.ipynb

## 前言

#### 抛弃Python 2，投靠Python 3
虽然几乎目前所有主要的开源 Python 包现在都同时支持 Python 3.x 和 Python 2.7；但Python 2.7 将于 2020 年退休，已陆续有一大批 Python 项目宣布将在 2020 年之前放弃对 Python 2.7 的支持，包括 pandas、Zulip、IPython、NumPy 等等
参见：https://python3statement.org/

#### 关于channel
channel是conda的一个独特的概念，（独特是指，在pip中没有这个概念），channel就是分发渠道的意思，你可以理解为是一些conda包的集合。一个package在不同的channel可以共用同一名称，但是可以提供不同的内容。比如同一款包，其作也许会在某个channel会分发商用的版本，而在其他的channel中发布免费版。conda有几个主要的channel如free, main, pro, conda-forge。前面三个由anaconda背后的continuum自己维护，因此anaconda又把这三个channel并在一起成了一个大的Anaconda Repository(repository的概念和channel一致)。当前，pro这个channel已经决定要淡出。详见https://repo.continuum.io/pkgs/


## Ubuntu的Python
```
sudo python3 -m pip uninstall pip && sudo apt install python3-pip --reinstall
python3 -m pip install -i https://pypi.tuna.tsinghua.edu.cn/simple pip -U
```

把/usr/bin/pip3
```
import sys
from pip import main
if __name__ == '__main__':
     sys.exit(main())
```     
     
改为:
```
import sys
from pip import __main__
if __name__ == '__main__':
     sys.exit(__main__._main())
```
注意，最后一个main()函数前有一个underscore..



## Install and configure Anaconda 
1.  Download and install Anaconda from TUNA's mirror 从 TUNA 的镜像下载和安装 Anaconda
    1.  Visit 访问 https://mirrors.tuna.tsinghua.edu.cn/anaconda/archive/
    1.  Choose the Anaconda version (preferrably the latest one), and pick up the version that matches your OS. 先选择Anaconda的版本（建议选择最新的，页面的最下方），并且选择与自己操作系统对应的版本
        1.  As of writing this instruction, the latest version is 2019.03. For Windows users, you can choose  [Anaconda3-2019.03-Windows-x86_64.exe](https://mirrors.tuna.tsinghua.edu.cn/anaconda/archive/Anaconda3-2019.03-Windows-x86_64.exe)
    1.  Download and install it 下载安装之


1.  Setup channels 设置相应的“通道”，下载和安装

    说明：Anaconda 的 `conda` 命令是一个类似于 `pip` 的第三方包管理器，里面有“channel（通道）”这种概念，所谓的通道，就是一组包名和相应的来源网址。Anaconda在刚安装完成时，默认是从官方网站下载，这样会导致速度比较慢。我们可以将其设置为TUNA的通道，这样就会快很多。

    1.  Start menu, locate and right-mouse-click “Anaconda Prompt” -> “Run as Administrator” 

        开始菜单，找到“Anaconda Prompt”并右键->“以管理员运行”

    1.  Run the following commands

    执行下列命令（注意，这期间有可能会中断或者提示，请留意相应的信息）

        pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple

        python -m pip install -U --force-reinstall pip

        conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
        conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
        
        :: (Deprecated "pro" channel)
        :: conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/pro/

        :: (Optional) Use conda-forge channel 
        :: conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge/
        
        conda config --set show_channel_urls yes
        
        conda update -y conda anaconda
                
        conda update -y jupyter numpy sympy scipy matplotlib
        
        conda install -y jupyterlab
        
        :: (Optional) Run the following lines of code
        :: pip install --upgrade requests 
        :: pip install --upgrade pandas pandas-datareader  
        :: pip install --upgrade pillow
        :: pip install sklearn

### Install Kite 
[kite](https://kite.com/) is an AI-powered Python co-pilot. It integrates with most Python code editors and uses machine learning to
turbocharge the programming experience.
* Download: https://kite.com/download
* Pycharm Plugin: https://github.com/kiteco/plugins/tree/master/intellij
* VS Code Plugin: https://github.com/kiteco/plugins/tree/master/vscode

### Install PyTorch

    conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/pytorch/
    conda install pytorch
    pip install torchvision

### Install Tensorflow

  * __方法1) pip方式：__
     
     操作：在将pip设置成指向TUNA或其他相对比较快的仓库后，运行`pip install tensorflow`或`pip install tensorflow-gpu`

  * __方法2) msi/exe方式：（适合Windows）__
  
     操作：去 https://www.lfd.uci.edu/~gohlke/pythonlibs/#tensorflow 下载安装文件，并在本地安装

  * __方法3) 手动安装方式：（适合Linux, MacOS, 及Windows）__
     
     操作：先访问 https://mirrors.tuna.tsinghua.edu.cn/tensorflow/ ，找到与自己系统对应的版本的路径，然后下载相应的.whl文件，最后再在本地执行`pip install some-package.whl` 
     
     不推荐的原因：TensorFlow已经移至PyPI，也就是说TUNA的PyPI镜像已经自动包括了tensorflow，而这个专门的tensorflow不再被维护和更新，只是因历史遗留问题存在。
     
  * __方法4) conda方式（不推荐）：__
     
     方法：执行`conda install tensorflow-gpu`或`conda install tensorflow`        

     不推荐的原因：如果用conda更新，有可能像[这里](https://www.reddit.com/r/tensorflow/comments/9qlo2s/anaconda_stuck_on_windows/)一样，在“Solving Environment”那里死住出不来，即使禁用Windows Defender也没用。
      
        
### Install Caffee
    conda install caffe-gpu

### Install MxNet
    conda install mxnet-gpu


### Change the Jupyter start-up folder

If you're using a Windows System, you might encouter difficulties in setting the default path for Jupyter Notebook. Current information available online is pretty scattered. Below there is a working solution tested by me. 

1.  Add it to the global config file
    1.  Open "Anaconda Prompt" and type `jupyter notebook --generate-config`, and press `y+Enter` to confirm
    1.  Find the file in `C:\Users\username\.jupyter\jupyter_notebook_config.py`
    1.  Change the line of `#c.NotebookApp.notebook_dir = ''` to `c.NotebookApp.notebook_dir = 'c:\\your\\workbench\\'`
        1.  Remeber to remove the comment hashbang `#`
        1.  Here, there should be double slashes, since single `\` means escaping
1.  Then, change the shortcut of Jupyter Notebook
    1.  go to `C:\ProgramData\Microsoft\Windows\Start Menu\Programs\Anaconda3 (64-bit)`, right-mouse-click the "Jupyter Notebook" shortcut icon and open "Properties" dialog
    1.  In the Target field, remove `%USERPROFILE%`
    1.  In the field of "Start in", type the same directory of `c:\your\workbench\` as abovementioned.
1.  Done!

## Jupyter Extensions

### jupyterlab-latex
https://github.com/jupyterlab/jupyterlab-latex

### Microsoft Word / .docx file exporter
https://github.com/m-rossi/jupyter-docx-bundler

### Jupytext
Jupyter notebooks as Markdown documents, Julia, Python or R scripts.
* https://github.com/mwouts/jupytext
* https://github.com/mwouts/jupyterlab-jupytext
* https://mybinder.org/v2/gh/mwouts/jupytext/master?urlpath=lab/tree/demo/get_started.ipynb
* https://towardsdatascience.com/introducing-jupytext-9234fdff6c57

### jupyterlab-drawio
A standalone embedding of the FOSS draw.io / mxgraph package into jupyterlab
* https://github.com/QuantStack/jupyterlab-drawio
* https://blog.jupyter.org/a-diagram-editor-for-jupyterlab-a254121ff919


