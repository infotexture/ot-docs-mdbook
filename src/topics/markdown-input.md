# Markdown input

[Markdown](https://daringfireball.net/projects/markdown/) is a lightweight markup language that allows you to write using an easy-to-read plain text format and convert to structurally valid markup as necessary.

In the words of its creators:

> “The overriding design goal for Markdown’s formatting syntax is to make it as readable as possible. The idea is that a Markdown-formatted document should be publishable as-is, as plain text, without looking like it’s been marked up with tags or formatting instructions.”

DITA Open Toolkit allows you to use Markdown files directly in topic references and export DITA content as Markdown.

These features enable lightweight authoring scenarios that allow subject matter experts to contribute to DITA publications without writing in XML, and support publishing workflows that include DITA content in Markdown-based publishing systems.

## Adding Markdown topics

In 2015, the original DITA-OT Markdown plug-in introduced a series of conventions to convert Markdown content to DITA, and vice-versa. This Markdown flavor was called [Markdown DITA](../reference/markdown/Markdown-DITA-syntax.md). The `markdown` format adds several complementary constructs to represent DITA content in Markdown, beyond those proposed for the [MDITA](../reference/markdown/MDITA-syntax.md) format in the [Lightweight DITA](lwdita-input.md) specification drafts.

**Tip:** For details on the differences in [Markdown formats](../reference/markdown-formats.md), see [Markdown DITA syntax](../resources/../reference/markdown/Markdown-DITA-syntax.md), [MDITA syntax](../resources/../reference/markdown/MDITA-syntax.md), and [Format comparison](../reference/markdown/Format-comparison.md).

To add a Markdown topic to a DITA publication, create a topic reference in your map and set the `@format` attribute to `markdown` so the toolkit will recognize the source file as Markdown and convert it to DITA:

```
<?xml version="1.0" encoding="utf-8"?>
<!DOCTYPE map PUBLIC "-//OASIS//DTD DITA Map//EN" "map.dtd">
<map>
  <topicref href="markdown-dita-topic.md" **format="markdown"**/>
</map>
```

When you add Markdown topics to a DITA publication as described above, the content is temporarily converted to DITA in the background when generating other output formats like HTML or PDF, but the Markdown source files remain unchanged.

**Tip:** This approach is recommended in cases where simple content is authored collaboratively over multiple versions, as Markdown topics can be edited by a wide range of authors and combined as necessary with more complex content maintained in DITA XML.

## Converting Markdown to DITA

In cases where the Markdown input is a one-off contribution, members of the DITA authoring team can use the Markdown file as raw material that is easily converted to DITA and enriched with conditional processing attributes, conkeyrefs or other more complex semantics that have no equivalent in limited formats like Markdown.

If you prefer to maintain this content in DITA in the future, you can generate DITA output by passing the **--format**=dita option on the command line.

This converts all input files \(both DITA XML and Markdown\) to [Normalized DITA](dita2dita.md). You can then copy the generated DITA files from the output folder to your project and replace references to the Markdown topics with their DITA equivalents.

**Related information**  


[Generating Markdown output](../topics/dita2markdown.md)

[Markdown plugin](https://www.oxygenxml.com/events/2015/dita-ot_day.html#Markdown_plugin)

**Targetonly**  


[Markdown DITA syntax](../reference/markdown/Markdown-DITA-syntax.md)

