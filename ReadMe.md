# DITA Open Toolkit Markdown Demonstration

This repository includes a snapshot of the [DITA Open Toolkit][1] documentation in [Markdown][2] format.

The output was generated using the [Lightweight DITA plug-in][3] for DITA-OT and published via [mdBook][4] to illustrate the capabilities of modern collaboration and publishing toolchains based on Markdown and how they may be combined with DITA content.

## Sample mdBook output

The Markdown source files in this repository were rendered to mdBook’s default static website output via the `mdbook` [command line interface][5].

The demonstration output is available on the GitHub project site at [infotexture.github.io/ot-docs-mdbook][6].

The content was generated from the [DITA-OT 3.6 docs][7] as hosted on the _DITA Open Toolkit_ project website at [www.dita-ot.org/3.6/][8].

## Reporting issues

Since plain-text formats like Markdown are inherently simple, they cannot represent the full range of semantics encoded in DITA content, so some information is lost in translation when exporting DITA content to Markdown.

With that in mind, if you see errors in the exported Markdown or have suggestions on enhancing the Markdown conversion routine, please submit them to [jelovirt/org.lwdita/issues][9].

If you notice issues in the content of the docs themselves, please report them via [dita-ot/docs/issues][10].

[1]: http://www.dita-ot.org
[2]: http://daringfireball.net/projects/markdown/
[3]: https://github.com/jelovirt/org.lwdita
[4]: https://rust-lang.github.io/mdBook/
[5]: https://rust-lang.github.io/mdBook/cli/
[6]: https://infotexture.github.io/ot-docs-mdbook
[7]: https://github.com/dita-ot/docs/tree/3.6
[8]: https://www.dita-ot.org/3.6/
[9]: https://github.com/jelovirt/org.lwdita/issues
[10]: https://github.com/dita-ot/docs/issues
