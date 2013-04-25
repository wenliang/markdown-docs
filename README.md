# Markdoc - Documentation generator for Markdown projects

Markdoc is a documentation generator for projects using Markdown. The problem with having Markdown files spread around your project is that it is hard to get an overview of all your documentation. Markdoc solves this by collecting all of your Markdown files into one browsable HTML hierarchy.

## Usage

### Browsing docs with the embedded web server

Run the following to fire up a local web server with your documentation

    cd your/project/path
    markdoc

or

    markdoc serve

Then point your browser to [http://localhost:5000/](http://localhost:5000/).

### Generating HTML output

    cd your/project/path
    markdoc generate --output ~/docs

If you do not set `--output` a temporary directory will be created for you.


## Installation

The easiest way is to install Markdoc via `pip`

    pip install markdoc

## Features

- Quick overview of all project Markdown files
- Adding [Table of contents](http://pythonhosted.org/Markdown/extensions/toc.html)
- [Syntax highlighting](http://pythonhosted.org/Markdown/extensions/code_hilite.html)
- Reads title from [metadata](http://pythonhosted.org/Markdown/extensions/meta_data.html)
- Support for the [Markdown tables extension](http://pythonhosted.org/Markdown/extensions/tables.html)
- No Internet connection needed
- Markdoc comes with an embedded web server for serving static HTML locally

### Metadata details

Markdoc is looking for Markdown meta data. Currently Markdoc is only taking the `Title` meta data attribute in consideration. Meta data in Markdown looks like this

    Title: Document title
    Date: 2013-04-25

    This is where my Markdown really starts

Using meta data in Markdoc is optional. If the `Title` tag is there, Markdoc will show that document title instead of the file name on the index page.

### Syntax highlighting

Markdoc supports syntax highlighting via the `Markdown` module. You can define the programming language by adding `:::language` as in this example

    :::python
    print('This is highlighted as Python code')

More details can be found in the [module docs](http://pythonhosted.org/Markdown/extensions/code_hilite.html).

### Adding Table of contents

A table of contents will be automatically generated in the HTML output if Markdoc finds a `[TOC]` tag anywhere in the Markdown.

    # Table of contents

    [TOC]

    # My header

    ## My subheader

Author
------

This project is maintained by [Sebastian Dahlgren](http://www.sebastiandahlgren.se) ([GitHub](https://github.com/sebdah) | [Twitter](https://twitter.com/sebdah) | [LinkedIn](http://www.linkedin.com/in/sebastiandahlgren))

License
-------

APACHE LICENSE 2.0
Copyright 2013 Sebastian Dahlgren

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.