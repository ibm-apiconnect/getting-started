---
title: Installing API Connect Developer Toolkit
toc: false
keywords:
sidebar: gs_sidebar
permalink: /Install.html
summary: Developer Toolkit includes the apic command-line tool and the API Designer visual tool
---

## Install Node

If you haven’t already done so, [install Node.js](https://nodejs.org/en/download/).

{% include note.html content="API Connect supports the current Node.js long-term support (LTS) version, but we expect it to run on more recent Node versions as well, though they may not yet be officially supported.
" %}

### Windows

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

## Install API Connect Developer Toolkit

On all platforms, enter this command to install the Developer Toolkit from npm:

```
$ npm install -g apiconnect
```

This installs:

- The `apic` command-line tool.
- The API Designer visual tool.
- API Connect Micro Gateway.
