# Smartduck docs

This is the documentation for the smartduck web-application.
Smartduck is a demo web-application of AI-enhanced Climate Science.

This documentation is written using [Jupyter Book](https://jupyterbook.org/intro.html).

## Installation

Get source from GitHub:
```
$ git clone https://github.com/FREVA-CLINT/smartduck-docs.git
$ cd smartduck-docs
```

Create conda environment:
```
$ conda env create -f environment.yml
$ conda activate smartduck-docs
```

## Build docs

Build HTML pages locally:
```
$ jupyter-book build book
```

Open generated docs in firefox:
```
$ firefox book/_build/html/index.html
```
