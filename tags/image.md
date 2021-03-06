---
layout: document
category: Tags
published: true
title: Image
description: Tag that Textpattern will replace with an 'img' HTML tag matching an image uploaded via the Images panel.
tags:
  - Image tags
---

# Image

On this page:

* [Syntax](#syntax)
* [Attributes](#attributes)
* [Examples](#examples)
* [Genealogy](#genealogy)

## Syntax

~~~ html
<txp:image />
~~~

The **image** tag is a *single* tag that Textpattern will replace with the `<img src="…">` HTML tag matching the image of the numeric `id` assigned by Textpattern when the image was uploaded via the Textpattern [Images panel](https://docs.textpattern.com/administration/images-panel).

The tag outputs the `alt`, `width`, and `height` attributes by default. If you don't need to set image dimensions (e.g. if you use `width: 100%` in your CSS), you can 'turn off' the effect of the `width` and `height` attributes by using `width="0" height="0"`.

The tag is also context-sensitive: if an `id` or `name` attribute is not specified, it can be used inside an [images](images) tag or form to output an `<img src="…">` HTML tag matching the current image.

## Attributes

Tag will accept the following attributes (**case-sensitive**):

`escape="html"` <span class="footnote warning">v4.0.4+</span>
: Escape [HTML entities](https://developer.mozilla.org/en-US/docs/Glossary/Entity) such as `<`, `>` and `&` for the image's `alt` and `title` attributes.
: **Values:** See the [tag escaping](https://docs.textpattern.com/tags/tag-basics/tag-escaping) documentation for all possible values.
: **Default:** `html`.

`height="integer"` <span class="footnote warning">v4.3.0+</span>
: Specify an image `height` which overrides the value stored in the database. Use `height="0"` to turn off the output of a width attribute in the `<img>` tag (thus the browser will scale the height if a width is used).
: **Default:** height of image stored in the database.

`html_id="id"` <span class="footnote warning">v4.0.4+</span>
: The HTML `id` attribute applied to the `wraptag`, if set, otherwise to the `<img>` tag.
: **Default:** unset.

`id="integer"`
: Specifies the `id`, assigned at upload of the image, to display. Can be found on the [Images panel](https://docs.textpattern.com/administration/images-panel). If both `name` and `id` are specified, `name` is used while `id` is ignored. If neither is specified, the tag must be used within an [images](images) tag or form.

`name="image name"`
: Specifies which image to display by its image `name` as shown on the [Images panel](https://docs.textpattern.com/administration/images-panel).

`width="integer"` <span class="footnote warning">v4.3.0+</span>
: Specify an image `width` which overrides the value stored in the database. Use `width="0"` to turn off the output of a width attribute in the `<img>` tag (thus the browser will scale the width if a height is used).
: **Default:** width of image stored in the database.

### Common presentational attributes

These attributes, which affect presentation, are shared by many tags. Note that default values can vary among tags.

`class="class name"`
: HTML `class` to apply to the `wraptag` attribute value, if set, otherwise to the `<img>` tag.
: **Default:** unset (see [class cross-reference](https://docs.textpattern.com/tags/tag-attributes-cross-reference#class)).

`style="style rule"`
: Inline CSS `style` rule. It's recommended that you assign CSS rules via `class` attribute instead.
: **Default:** unset.

`wraptag="element"` <span class="footnote warning">v4.0.4+</span>
: HTML tag to be used to wrap the `<img>` tag, specified without brackets (e.g. `wraptag="ul"`).
: **Default:** unset (but see [wraptag cross-reference](https://docs.textpattern.com/tags/tag-attributes-cross-reference#wraptag) for exceptions).

## Examples

### Example 1: Display the given image

~~~ html
<txp:image id="42" />
~~~

Displays the image uploaded as ID #42.

### Example 2: Apply a CSS class

~~~ html
<txp:image name="chickens.jpg" class="promoted" />
~~~

Displays the image named `chickens.jpg` and assigns a `class="promoted"` attribute/value to the `<img>` tag.

Had the `wraptag` attribute been used, the `class="promoted"` attribute/value would have been applied to that instead of directly to the image tag.

### Example 3: Use within images tag

~~~ html
<txp:images>
    <txp:image />
</txp:images>
~~~

Displays full-size images for all images found by the [images](images) tag.

## Genealogy

### Version 4.3.0

`height` and `width` attributes added. \\
Added context sensitivity within [images](images) tag.

### Version 4.2.0

`align` attribute deprecated.

### Version 4.0.7

Default value for `escape` attribute changed from 'unset' to `html`.

### Version 4.0.4

`escape`, `html_id` and `wraptag` attributes added.
