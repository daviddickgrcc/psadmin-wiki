---
title: Style Guide
layout: en
permalink: /style_guide/
---

# psadmin.io Community Wiki Style Guide

(Copied from the Travis CI documentation style guide - it's realy good.)

## Markdown and structure

### Headings

For historical reasons, the top level heading in Jekyll markdown files is level 2 (##) not level 1 (#).

We use ATX style headings, and do not use the optional closing hashes:

```markdown
## This is an H2

### This is an H3

#### This is an H4
```

We do not use underline style headings:

```markdown
Do not use this style heading
=============================
```

### Lists

If you have long lists you can wrap them into 2 (`.column-2`) or 3 (`.column-3`) columns using one of the follow CSS classes after your list item:

```css
* long list item 1
* long list item 2
{: .column-2 }
```

### TOC

Add a table of contents to a page with the following HTML snippet:

```html
<div id="toc"></div>
```

### Beta features

Mark all beta features with a specially formatted note. Both the `> BETA` and
the `{: beta}` are required.

> BETA Awesome new feature that might not be enabled and is subject to change.
{: .beta}

### GUI

Make sure all references to items in a GUI match the case of the UI, and are marked with *asterisks*.

### Links

Make sure all links have titles:

```markdown
The [link][example1] in the text

[example1]: http://www.example.com  "Example URL"
```

or

```markdown
The [link](http://www.example.com "Example URL") in the text
```

### Code Inline

All function names, filenames, etc should be marked with `back-ticks`.

If you're talking about applications or services, only the actual command should be marked as code, not the name of the service:

- Start SQL*Plus by running `sqlplus`.

### Blockquotes / Notes / Warnings

Use `>` to indicate notes and warnings:

```markdown
> Note this important info!

```

### Code blocks

Code blocks should be fenced with triple back-ticks "\`\`\`" and named according to [prism.js][prism] for syntax highlighting.

[prism]: http://prismjs.com/#languages-list "Prism language list"

```markdown
your code here
```

You can also set the filename for a code block by adding a Kramdown attribute after it:

```markdown
This code is in .travis.yml
```
{: data-file=".travis.yml"}


## Images

Always include text for configuration items. Screenshots and images should only be used to accompany the text description; never use only an image for documentation.