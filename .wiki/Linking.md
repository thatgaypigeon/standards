# Linking
Linking should follow the standard syntax of `[Title](url)`. It should look like this: [Link](https://example.com).

## Linking to sections
Section links should include the section title in the display text, separated by a section sign and a non-breaking space on the right: `[Title § Section](url#section)`. It should look like this: [Example § Section](https://example.com#section).

## Linking to subpages
Subpage or inner links should include the main and subpage titles in the display text, separated by an arrow and a non-breaking space on the right: `[Title → Subpage](url)`. It should look like this: [Example → Subpage](https://example.com).

## Linking footnotes
To cite a footnotes, use `[^N]`, where `N` is a positive integer. It should look like this: [^1].

To explain a footnote, use `[^N]: text`.

## Linking sources
When using extracts from sources, use HTML markup to allow for indents:
```
> Extracted text here.
<dl><dd>⨽ Taken from <a href="url">Text</a></dd></dl>
```

It should look like this:

> **Number theory** (or **arithmetic** or **higher arithmetic** in older usage) is a branch of pure mathematics devoted primarily to the study of the integers and arithmetic functions.
<dd>⨽ Taken from <a href="https://en.wikipedia.org/wiki/Number_theory">Wikipedia: Number theory</a></dd>
