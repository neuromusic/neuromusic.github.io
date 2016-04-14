---
layout: post
title: "Moving from Matlab to Python: Where's my IDE?"
tags:
    - python
    - data science
    - science
    - matlab
    - jupyter
disqus: True
---

It seems that one of the first challenges for Matlab users who want to get started with Python isn't the language, but simply getting a development environment setup. Matlab eases onboarding through a single self-contained IDE. While there are IDEs for Python, I haven't been happy with any of them. Instead, this is my development stack and the basic setup I recommend for new Python users.

## Anaconda for Python & Package Management

To install Python and packages, I use the [Ananconda Python distribution](https://docs.continuum.io/anaconda/index).

It works great across Windows, Linux, and Mac (though there are some quirks on Windows).

Anaconda is nice because it handles all of the complex C & fortran compilation needed for scientific computing really nicely.

It also comes with a command line utility called "conda" that (a) [connects to their own package registry](http://conda.pydata.org/docs/using/pkgs.html) and (b) lets you [run multiple environments](http://conda.pydata.org/docs/using/envs.html) so you can isolate projects from each other, each with their own dependencies.

[Download Anaconda](https://www.continuum.io/downloads)

## Jupyter & IPython for Exploratory Analysis

Formerly called IPython, Jupyter is a browser-based interactive shell. You write and execute code in "cells"... the output shows up below each cell. You can reorder them or add a block of text. Then you can save the "notebook" file and send it to someone else to execute and explore. 

I use this for exploring data, much as I would use the command line or "cell mode" in Matlab. 

Once you start using it, Jupyter is extra awesome because you can do things like connect to your lab server installation from you browser while flying on an airplane with WAY less bandwidth than X11 forwarding or VNC. Jupyter is also language-agnostic, so you can run Julia, R, or even Matlab in Jupyter notebooks.

[Get started with Jupyter](http://jupyter.readthedocs.org/en/latest/install.html)

## Sublime Text for File Editing

The time will come when you need to write a `.py` file.

- You need to write a script to run on a server or overnight
- You need a local file to hold some common helper functions for a project
- You need to develop a package to be imported in multiple notebooks or scripts

For any of these, you need a text editor. Ostensibly, any text editor will do, but [Sublime Text](https://www.sublimetext.com/) and [Atom](https://atom.io/) are very popular as they offer lots of features out of the box that make programming in Python nice (e.g. code completion, syntax highlighting, and smart indentation), and offer plugin systems to do even more (like unit testing and git integration).

[Check out Sublime Text](https://www.sublimetext.com/)

If you *really* need an IDE, there are options. I've heard very good things about [PyCharm](https://www.jetbrains.com/pycharm/) though I find it slow on Ubuntu and [Rodeo](http://blog.yhat.com/posts/rodeo-native.html) looks promising depite being quite bloated. For now, I'm quite happy with the Jupyter+Sublime combo.