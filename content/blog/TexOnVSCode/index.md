---
title: 'LaTeX on VSCode (MacOS)'
summary: My first try on configuring LaTeX on VSCode on MacOS.
date: 2024-10-15
authors:
  - admin
tags:
  - LaTex
---

The first try on configuring LaTeX on VSCode on MacOS.

I've been using LaTeX for a while now, such as writing papers and modifying my CV on [Overleaf](https://www.overleaf.com). But it could be *kind of* slow and boresome to compile the document every time I make a change, which usually takes several seconds. Sometimes some bugs jump out after several compilations and force me to refresh the browser.

So, I decided to try out compiling the LaTeX documents locally by [VSCode](https://code.visualstudio.com/) on my Mac Air(M1).[^2][^3][^4]

## 1 Installing LaTeX Environment

The first step is to install LaTeX compilers, of which I have found several derivative versions. The version suitable for MacOs is **MacTeX**[^1] (>3G) or a smaller version **BasicTeX** (about 90M), both can be installed by `brew` directly. 

> **BasicTeX** supports typesetting standard teX and LaTeX documents, while **MacTeX** includes essentially *all* software available for typesetting with teX-like systems.[^1]
> The relation between the two is like **Anaconda** and **Miniconda** in Python environment management.

```bash
# MacTeX
brew install --cask mactex-no-gui   # without GUI
brew install --cask mactex          # I've installed MacTeX with this and it'll take a while to download and install.
# BasicTeX
brew install --cask basictex
```

Then the TeX will be installed in the following paths:
```
/etc/paths.d/TeX
/Library/TeX
/usr/local/texlive/2024
```

> **Notes**: the installation may request your *root password* to run `sudo`. After that, it looks stuck, but it's running installation *behind the terminal*. You can have a look at the paths previously shown to check whether there are some new files.

We can check the installation by running these commands in the terminal:
```bash
# check the version
pdftex --version
xelatex --version
# check the installation path
which pdftex    # /Library/TeX/texbin/pdftex
which xelatex   # /Library/TeX/texbin/xelatex
```

So it turns out that the **executable files** are in `/Library/TeX/texbin/`. If it doesn't output like that, execute `$PATH` to check whether the path is well-prepared, otherwise, we need to add it to the `PATH` to make it available in the terminal.

```bash
export PATH=$PATH:/Library/TeX/texbin # add the path to the PATH environment variable
```

Or we can also edit the `~/.bash_profile`, add the above line to its end, and run `source ~/.bash_profile` to make the change effective.

## 2 Configuring VSCode

The next step is to configure VSCode to use the LaTeX compiler we just installed. Here I used the extension [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop), by searching and installing it from the extension panel.


Click the gear icon `⚙️` in the bottom left, and click `Settings` to open the settings page, where we can open the `settings.json` by clicking the "Open settings file" button in the top right. Then we can edit the `settings.json` file directly by adding the following lines:
```json
{
    // previous content
    
    // LaTeX
    // Don't comnplle automatically after saving
    "latex-workshop.latex.autoBuild.run": "never",
    // Tools for compilation
    "latex-workshop.latex.tools": [
        {
            "name": "xelatex",
            "command": "xelatex",
            "args": [
                "-synctex=1",
                "-interaction=nonstopmode",
                "-file-line-error",
                "-pdf",
                "%DOCFILE%"
            ]
        },
        {
            "name": "pdflatex",
            "command": "pdflatex",
            "args": [
                "-synctex=1",
                "-interaction=nonstopmode",
                "-file-line-error",
                "%DOCFILE%"
            ]
        },
        {
            "name": "bibtex",
            "command": "bibtex",
            "args": [
                "%DOCFILE%"
            ]
        }
    ],
    // Recipes for compilation
    "latex-workshop.latex.recipes": [
        {
            "name": "xelatex",
            "tools": [
                "xelatex"
            ],
        },
        {
            "name": "xelatex*2",
            "tools": [
                "xelatex",
                "xelatex"
            ],
        },
        {
            "name": "pdflatex",
            "tools": [
                "pdflatex"
            ]
        },
        {
            "name": "xe->bib->xe->xe",
            "tools": [
                "xelatex",
                "bibtex",
                "xelatex",
                "xelatex"
            ]
        },
        {
            "name": "pdf->bib->pdf->pdf",
            "tools": [
                "pdflatex",
                "bibtex",
                "pdflatex",
                "pdflatex"
            ]
        }
    ],
}
```

Finally, **restart** VSCode to apply the changes.

## 3 Test

Now we can test the configuration by creating a new `.tex` file and writing some content. 
```tex
\documentclass{article}
\usepackage{amsmath}

\title{A Simple \LaTeX{} Document}
\author{Your Name}
\date{\today}

\begin{document}
\maketitle

\section{Introduction}
Welcome to the world of \LaTeX{}! With \LaTeX{}, you can create beautifully formatted documents with ease. Here's a simple example of a \LaTeX{} document.

\section{Mathematics}
\LaTeX{} excels at typesetting mathematical equations. For example, here's the quadratic formula:

\begin{equation}
  x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
\end{equation}

\end{document}
```

Then we can click the `Compile LaTeX Project` button in the left sidebar to compile the `.tex` file.

## 4 Others

- There are several **recipes** for compilation in the `settings.json` file, which may fit different kinds of documents. It's recommended to write a magic line at the beginning of the document:
  ```tex
  % !TEX program = xelatex
  ```
  If you wanna change the default recipe, or wanna change the order of the recipes, you can do it by modifying the `settings.json` file.
- For papers that use **Bibtex** for reference, you can use the `pdf->bib->pdf->pdf` recipe.



## Reference

[^1]: [MacTex](https://www.tug.org/mactex/)
[^2]: [LaTeX之一：macos上latex环境搭建（homebrew安装+vscode配置+ MacTex）和B站视频、网站、教程等相关资料推荐（Overleaf、公式预览网站）](https://blog.csdn.net/zhiaidaidai/article/details/140440448?fromshare=blogdetail&sharetype=blogdetail&sharerId=140440448&sharerefer=PC&sharesource=m0_61333822&sharefrom=from_link)
[^3]: [使用 VSCode 编写 LaTeX — Mac 篇](https://zhouyuqian.com/2020/12/09/TexOnVsCode/)
[^4]: [LaTeX知识库 - 帮助](https://www.latexstudio.net/LearnLaTeX/help.html)