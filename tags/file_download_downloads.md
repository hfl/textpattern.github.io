---
layout: document
category: Tags
published: true
title: File download downloads
description: The file_download_downloads tag will replace with the number of times the current file has been downloaded.
tags:
  - File tags
---

# File download downloads

On this page:

* [Syntax](#syntax)
* [Attributes](#attributes)
* [Examples](#examples)

## Syntax

~~~ html
<txp:file_download_downloads />
~~~

The **file_download_downloads** tag is a *single* tag that Textpattern will replace with the number of times the current file has been downloaded. Should be used in Textpattern 'file' type [Form templates](https://docs.textpattern.com/themes/form-templates-explained).

## Attributes

This tag has no attributes.

## Examples

### Example 1: Display the number of downloads

~~~ html
<p>
    Downloads:
    <txp:file_download_downloads />
</p>
~~~

### Example 2: Display the number of downloads of a particular file

~~~ html
<txp:file_download_list id="1">
    <p>
        <txp:file_download_name />
        downloaded
        <txp:file_download_downloads />
        times.
    </p>
</txp:file_download_list>
~~~

Other tags used: [file_download_list](file_download_list), [file_download_name](file_download_name).
