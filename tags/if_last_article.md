---
layout: document
category: Tags
published: true
title: If last article
description: The if_last_article tag will execute the contained statements if the displayed article is the last in the list.
tags:
  - Article tags
---

# If last article

On this page:

* [Syntax](#syntax)
* [Attributes](#attributes)
* [Examples](#examples)

## Syntax

~~~ html
<txp:if_last_article>
~~~

The **if_last_article** tag is a *conditional* tag and always used as an opening and closing pair, like this…

~~~ html
<txp:if_last_article>
    …conditional statement…
</txp:if_last_article>
~~~

The tag will execute the contained statements if the displayed article is the last in the currently displayed list. It will display in both single article and article list modes. Should be used in Textpattern 'article' type [Form templates](https://docs.textpattern.com/themes/form-templates-explained).

## Attributes

This tag has no attributes.

## Examples

### Example 1: Add an image after the last article in a list

~~~ html
<h3>
    <txp:permlink>
        <txp:title />
    </txp:permlink>
    |
    <txp:posted />
    by
    <txp:author />
</h3>

<txp:body />
<txp:comments_invite wraptag="p" />

<txp:if_last_article>
    <img src="https://example.com/footer.jpg" alt="Footer">
</txp:if_last_article>
~~~

Other tags used: [permlink](permlink), [title](title), [posted](posted), [author](author), [body](body), [comments_invite](comments_invite).
