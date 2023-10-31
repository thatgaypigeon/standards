# Hatnotes
**Hatnotes**, are short notices placed at the top of a page or section. They are used to help readers/users locate a different "thing" (page, website, repository, etc.) if the one they are at is not the one they were looking for.

> ⨽ *Modified from [Wikipedia: WP:Hatnote](https://en.wikipedia.org/wiki/Wikipedia:Hatnote)*

They serve a variety of purposes, such as disambiguation, clarification, redirection, or to dispaly other important information such as a date or title notice.

While generally used with MediaWiki, they can be useful in other contexts, such as this. As this is not a MediaWiki-powered site, there aren't auto-generating templates, and any hatnotes need to be typed manually. However, you can mimic their appearance using common markdown syntax ([see below](#syntax)). Also [below](#types) are some common hatnotes that can be copy-pasted.

## Usage
You can read the [Wikipedia help article](https://en.wikipedia.org/wiki/Wikipedia:Hatnote) for specifics on how hatnotes are used on Wikimedia sites, but in general, stick to the following:
* Place them at the top of relevant pages or sections
* Keep them short and informative
* Include direct links to other pages/sites/etc.
* Use them to disambiguate or redirect; not as explanations or article content

### Syntax
The general syntax for a hatnote is to indent, italicise, and, where possible, shrink the text. Generally, a hatnote should come immediately follow a heading marker and be followed by an empty line-break.

To do this in a Markdown file, create a blockquote and italicise the text. Since small text (that aligns well in a blockquote) is a little more tedious, it can be ignored here.

```
# Section
> *Hatnote text here.*

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus ornare dui eu euismod semper. Fusce dictum dolor quis purus gravida, nec porttitor urna dignissim. Vestibulum iaculis enim sit amet dolor scelerisque interdum...
```

For a text file, simply indent the text with 2 spaces then add a line break.
```
Section
---------
  Hatnote text here.

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus ornare dui eu euismod semper. Fusce dictum dolor quis purus gravida, nec porttitor urna dignissim. Vestibulum iaculis enim sit amet dolor scelerisque interdum...
```

### Combining hatnotes

Hatnotes can be used along side other hatnotes, but it is important to recognise when and how hatnotes should be grouped. They can be combined in two ways:
<dl>
  <dt><b>Inline</b></dt>
    <dd><blockquote><i>This is hatnote 1. This is hatnote 2.</i></blockquote></dd>
    <p></p>
    <dd>This approach should be used when hatnotes serve the same purpose (mainly some combination of the "About", "For", and "Distinguish" hatnotes; see <a href="#types">below</a>).</dd>
    <p></p>
  <dt><b>Block</b></dt>
    <dd><blockquote><i>This is hatnote 1.<p></p>This is hatnote 2.</i></blockquote></dd>
    <p></p>
    <dd>This approach should be used when hatnotes serve different purposes. It is achieved by inserting an empty paragraph element (<code>&lt;p&gt;&lt;/p&gt;</code>) between the two lines.</dd>
    <p></p>
</dl>

Multiple hatnotes should share the same `<blockquote>` element.

## Types
Below are some examples of hatnotes and their uses. These are not MediaWiki specific.

The hatnotes listed below are often combined (sometimes into a single Wikimedia template), but have been separated here for simplicity and generalisation. Those found on Wikimedia sites may be modified or omitted entirely.

| Name        | Content | Usage | Notes |
| ----------- | ------- | ----- | ----- |
| `{{`[`About`](https://en.wikipedia.org/wiki/Template:About)`}}` | *This (article/repo/folder/etc.) is about \<topic>.* | Generally combined with either "For" or "Distinguish" in the same line. |  |
| `{{`[`For`](https://en.wikipedia.org/wiki/Template:For)`}}` | *For \<topic>, see [link].* |  | A generic version for wider disambiguation is:<blockquote>*For other uses, see [link].*</blockquote> |
| `{{`[`Distinguish`](https://en.wikipedia.org/wiki/Template:Distinguish)`}}` | *[It is] Not to be confused with [link].* |  | When combined with another hatnote inline, the wording changes from "Not" to "It is not". |
| `{{`[`Main`](https://en.wikipedia.org/wiki/Template:Main)`}}` | *Main (article/repo/folder/etc.): [link].* | Only used in sections that summarise a subject, linking to a more thorough or detailed coverage of the topic. |
| `{{`[`Further`](https://en.wikipedia.org/wiki/Template:Further)`}}` | *Further (information/help): [link].* |  |
| `{{`[`See also`](https://en.wikipedia.org/wiki/Template:See_also)`}}` | *See also: [link].* | For related topics or topics that may provide additional information or context. |

For more information on how to link a topic, see [Links](/../Links).

## Examples

### Wiki-style
> <h3>Apple</h3>
> <hr/>
> <blockquote><i>This article is about the fruit. For the company, see <a href="https://en.wikipedia.org/wiki/Apple Inc.">Apple Inc.</a>. For other uses, see <a href="https://en.wikipedia.org/wiki/Apple_(disambiguation)">Apple (disambiguation)</a>.</i></blockquote>
> <p></p>
> An <b>apple</b> is a round, edible <a href="https://en.wikipedia.org/wiki/Fruit">fruit</a> produced by an <b>apple tree</b> (<i>Malus domestica</i>). Apple <a href="https://en.wikipedia.org/wiki/Fruit_tree">trees</a> are <a href="https://en.wikipedia.org/wiki/Agriculture">cultivated</a> worldwide and are the most widely grown species in the <a href="https://en.wikipedia.org/wiki/Genus">genus</a> <a href="https://en.wikipedia.org/wiki/Malus">Malus</a>. The <a href="https://en.wikipedia.org/wiki/Tree">tree</a> originated in <a href="https://en.wikipedia.org/wiki/Central_Asia">Central Asia</a>, where its wild ancestor, <a href="https://en.wikipedia.org/wiki/Malus_sieversii">Malus sieversii</a>, is still found. Apple have been grown for thousands of years...

<p></p>

> <h3>Torus</h3>
> <hr/>
> <blockquote><i>Not to be confused with <a href="https://en.wikipedia.org/wiki/Taurus">Taurus</a>.</i>
> <p></p>
> <i>This article is about the surface. For the volume, see <a href="https://en.wikipedia.org/wiki/Solid torus">Solid torus</a>. For other uses, see <a href="https://en.wikipedia.org/wiki/Torus_(disambiguation)">Torus (disambiguation)</a>.</i></blockquote>
> <p></p>
> In <a href="https://en.wikipedia.org/wiki/Geometry">geometry</a>, a <b>torus</b> (<abbr title="plural form">PL</abbr>: <b>tori</b> or <b>toruses</b>) is a <a href="https://en.wikipedia.org/wiki/Surface_of_revolution">surface of revolution</a> generated by revolving a <a href="https://en.wikipedia.org/wiki/Circle">circle</a> in <a href="https://en.wikipedia.org/wiki/Three-dimensional_space">three-dimensional space</a> one full revolution about an axis that is <a href="https://en.wikipedia.org/wiki/Coplanarity">coplanar</a> with the circle. The main types of toruses include ring toruses, horn toruses, and spindle toruses. A ring torus is sometimes colloquially referred to as a <b>donut</b> or <b>doughnut</b>.

### Other uses
Of course, hatnotes can be used with any text for a wide variety of situations and contexts, as long as they are kept concise and follow the rules [above](#usage).

Below are some other examples that aren't used for disambiguation or redirection.

#### Lists

> *This is a dynamic list and may never be able to satisfy particular standards for completeness. You can help by suggesting additions to this list.*

Based on Wikipedia's [Template:Dynamic list](https://en.wikipedia.org/wiki/Template:Dynamic_list), this hatnote can be useful above "dynamic lists", such as [awesome lists](https://github.com/topics/awesome), lists of people, places, music, etc. Other dynamic lists are those which may be ongoing, changing, or too broad to ever be reasonably completed. Some examples include:
* Unsolved problems in mathematics — ongoing, changing
* Notable (people/places/etc.) — ongoing, changing, and subjective
* List of fictional countries — ongoing
* Lists of works — ongoing
  * Albums by \<musician>
  * TV shows by \<director>
  * Video games published by \<publisher>
  * Films nominated for Oscars
  * etc.
* People from (town/city/etc.) — too broad, notability is subjective

---

> *This list is incomplete. You can help by suggesting additions to it.*

Based on Wikipedia's [Template:Incomplete list](https://en.wikipedia.org/wiki/Template:Incomplete_list).

---

> *For a more comprehensive list, see [link].*

Based on Wikipedia's [Template:Main list](https://en.wikipedia.org/wiki/Template:Main_list).

#### Time

> *This page is up-to-date as of \<date>.*

For content that may change, such as hit counters, number of followers, etc.

---

> *This page is up-to-date as of \<version>.*

For content that may change with software versions, etc.

#### Other
Other common hatnotes include:
<dl>
  <dt><a href="https://en.wikipedia.org/wiki/Category:Correct_title_templates"><b>Correct title templates</b></a></dt>
    <dd><blockquote><i>The correct title of this page is &lt;title&gt;. It appears incorrectly here due to technical restrictions.</i></blockquote></dd>
    <p></p>
    <dd>Based on Wikipedia's <a href="https://en.wikipedia.org/wiki/Template:Correct_title">Template:Correct title</a>.</dd>
    <p></p>
  <dt><a href="https://en.wikipedia.org/wiki/Category:Hatnote_templates_for_names"><b>Name templates</b></a></dt>
    <dd><blockquote><i>In this &lt;language&gt; name, the surname is "&lt;name1&gt;", not "&lt;name2&gt;".</i></blockquote></dd>
    <p></p>
    <dd>Based on Wikipedia's <a href="https://en.wikipedia.org/wiki/Template:Family_name_hatnote">Template:Family name hatnote</a>.</dd>
    <p></p>
  <dt><b>Transclusion or source notices</b></dt>
    <dd><blockquote><i>(This/The below) section has been (transcluded/copied/modified) from &lt;source&gt;.</i></blockquote></dd>
    <p></p>
    <dd>Based on Wikipedia's <a href="https://en.wikipedia.org/wiki/Template:Transcluded_section">Template:Transcluded section</a>. See also <a href="/../Markdown#using-sources">Markdown § Using sources</a>.</dd>
    <p></p>
</dl>

The full list of hatnote templates used on Wikipedia can be found [here](https://en.wikipedia.org/wiki/Category:Hatnote_templates).
