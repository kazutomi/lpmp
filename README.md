# lpmp - Leanpub Markdown Preprocessor

## Usage

    $ lpmp [-v|--verb] [-d|--dump] [-s sep] [-h]

The command reads Book.txt and *.lmp files
and generates corresponding .txt or .md files.
If Book.txt has a '01.txt' (or '01.md') entry,
provide 01.lmp and run lpmp to produce 01.txt (or 01.md).

* `-s` or `--verb` : display verbatim lines for debug
* `-d` or `--dump` : display all lines under processing
* `-s sep` : separator for section names in index (default `.`)
* `-h` : show help

## Commands available in .lmp files

In addition to the Leanpub Markdown syntax, the following commands
are available in .lmp files.

- `@<kw>{word,yomi}` : keyword to be indexed (in boldface); yomi can be omitted
- `@<idx>{word,yomi}` : same as `@<kw>` but not boldface
- `@<hidx>{word,yomi}` : hidden index, not appear as text

Giving any third argument to `@<idx>` or `@<hidx>` makes the index entry boldface. (e.g., `@<idx>{foo,foo,1}`)

- `@<index>{}` : generates index
- `@<ruby>{word,furigana}` : give furigana
- `@<fig>{tag}[caption](file)` : insert image
- `@<fig>(tag)` : figure reference
- `@<tbl>{tag}[caption]` ... `@<tbl>` : table block
- `@<tbl>(tag)` : table reference
- `@<list>{tag}[caption](file)` : insert code
- `@<list>{tag}[caption]` ... `@<list>` : literal code block
- `@<list>(tag)` : list reference
- `@<lists>{}` : generates the list of lists
- `@<cmd>{option}` ... `@<cmd>` : command-line session
- `@<slabel>{tag}` : label the section
- `@<sref>(tag)` : reference to section
- `@<bib>{tag}` ... `@<bib>` : bibliography item
- `@<bib>(tag)` : reference to bib item

Captions can include `[...]` to one level (nested ones not allowed).

`@<fig>{`, `@<tbl>{` and `@<list>{` can take options at end
in `{...}` form: e.g., `@<list>{...}[...]{linenos=off}`

Do not add `#` in front of tags specified in `@<...>` commands;
they automatically add one if necessary.
