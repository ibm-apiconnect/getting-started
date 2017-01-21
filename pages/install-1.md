---
title: Install Node.js
keywords:
layout: tutorial
sidebar: install
permalink: /install-1.html
summary: You have to install Node.js before you can install the API Connect Developer Toolkit
---
## Install Node.js

If you haven’t already done so, [install Node.js](https://nodejs.org/en/download/).

{% include note.html content="API Connect supports the current Node.js long-term support (LTS) version, but we expect it to run on more recent Node versions as well, though they may not yet be officially supported.
" %}

## Windows

If you have a version of Node prior to 6.x, install version 3 of npm by entering the following command:

```
$ npm install -g npm
```

Then ensure the npm command uses the correct version:

```
$ npm -v
```

If the version shown is not 3.x.x, then edit your system PATH to ensure that `C:\Users\username\AppData\Roaming\npm` supersedes any other entries.
For more information, see the [Installing the toolkit in the Knowledge Center](http://www.ibm.com/support/knowledgecenter/SSMNED_5.0.0/com.ibm.apic.toolkit.doc/tapim_cli_install.html?lang=en).
