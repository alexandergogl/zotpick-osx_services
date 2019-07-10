# Zotpick OSX services

OSX services to run the Zotero [citation dialog](https://www.zotero.org/support/word_processor_plugin_usage) from a text editor.

Credits: Applescript by [David Smith](https://github.com/davepwsmith/zotpick-applescript) and idea for the workflow by [Raphael Kabo](http://raphaelkabo.com/blog/posts/markdown-to-word/).

Three workflows are available:

1. `zotpick-asciidoc.workflow` 
2. `zotpick-pandoc.workflow`
3. `zotpick-citekey.workflow`
4. `zotpick-zotero_quick_export`

There is also a workflow for [Alfred](https://www.alfredapp.com/):

1. `zotpick-zotero_quick_export.alfredworkflow`

## Installation

1. Download and install the applescript workflow with the format (Asciidoc or Markdown) you want to use and install it as a service.
2. Add a shortcut to the service (`System Preferences > Keyboard > Shortcuts > Services > zotpick-pandoc`)
3. Pushing the shortcut in a text editor will invoke the Zotero reference search command (Zotero has to run) and will add a citation like `@smith2018` if you have chosen the pandoc format.

## Background information

When Zotero is running the Zotero Better-BibTex (BBT) plugin exposes an URL at `http://localhost:23119/better-bibtex/cayw?format=`, where the format parameter can be set to a number of formats. See https://retorque.re/zotero-better-bibtex/cayw/ for more information.

The URL recognises the following better-bibtex citation formats (see also [zotero-better-bibtex](http://retorque.re/zotero-better-bibtex/citing/cayw/)):

* `pandoc`

* `mmd`

* `cite`

* `citet`

* `citep`

* `LaTex`

* and the bibtex citation key called `playground`
