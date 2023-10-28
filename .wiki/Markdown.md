# Markdown

## Headings
Headings containing a forward slash (`/`) should surround it with spaces (like / this, not/this).

## Footnotes & Citations
| Type | Description | Usage |
| ---- | ----------- | ----- |
| Footnote | A numbered link to the end of a page with an explanatory or additional note | Footnote<sup>[1](#footnote-1)</sup>, or <sup>[*](#footnote-1)</sup> |
| Note | Like a footnote, but they usually link to the end of a section instead | Note<sup>[a](#note-1)</sup>, or<sup>[[note 1]](#note-1)</sup> |
| Citation | A numbered link to a specific reference material | Citation<sup>[[1]](#citation-1)</sup> |
| Reference(s) | A list of referenced materials at the end of a page | <ol><li>Reference 1</li><li>Reference 2</li><li>Reference 3</li></ol> |

The "references" section should be a level 2 element at the bottom of the page. It should be titled "References", and there should be a 

For more information about where to place this section, see [page layout](https://github.com/thatgaypigeon/standards/wiki/Page-layout).

## Using sources
When using information from a source where an inline footnote is not appropriate (such as images/diagrams, lists, tables, etc.)

When using extracts from sources, use the following markup:
```
Extracted text here.
> ⨽ *Taken from [source](url)*
```

This uses the Unicode character **U+2A3D** (`⨽`) "Righthand Interior Product".

If the text has been modified, use the following markup instead:
```
Modified text here.
> ⨽ *Modified from [source](url)*
```

For this definition, "modified text" is any text that has had any of the following changes:
* Adding/removing/changing words or phrases
* Adding/removing/changing punctuation
* Removing a set of brackets and their contents

This does <u>not</u> include any of the following:
* Capitalisation differences
* Spelling differences
* Markup changes, such as emboldening or italicising text
* Removing links (but it does include adding links)
* Removing inline citations

It should look like this:

**Number theory** (or **arithmetic** or **higher arithmetic** in older usage) is a branch of pure mathematics devoted primarily to the study of the integers and arithmetic functions.
> ⨽ *Taken from [Wikipedia: Number theory](https://en.wikipedia.org/wiki/Number_theory)*

---
