---
layout: document
category: Tags
published: true
title: File download
description: The file_download tag will replace with a Textpattern 'file' type Form template.
tags:
  - File tags
---

# File download

On this page:

* [Syntax](#syntax)
* [Attributes](#attributes)
* [Examples](#examples)

## Syntax

~~~ html
<txp:file_download />
~~~

The **file_download** tag is a *single* tag which Textpattern will replace with Textpattern 'file' type [Form templates](https://docs.textpattern.com/themes/form-templates-explained). Inside that form go the other [file tags](https://docs.textpattern.com/tags/file-tags).

## Attributes

Tag will accept the following attributes (**case-sensitive**):

`filename="name"`
: Filename of the file to link to.
: **Default:** unset (nothing is returned).

`form="form name"`
: Use specified form template to process the files.
: **Default:** `files`.

`id="integer"`
: File `id` of the file to link to.
: **Default:** unset (nothing is returned).

## Examples

### Example 1: Display a download form

~~~ html
<txp:file_download form="new-files" id="1" />
~~~

Gets file with `id` of `1` and displays results using `new-files` form.
