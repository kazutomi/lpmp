# lpmp - Leanpub Markdown Preprocessor
--------

## Usage

    $ lpmp

The command reads Book.txt and *.lmp files
and generates corresponding .txt files.

## Commands available in .lmp files

- `@<kw>{word,yomi}` : keyword to be indexed; yomi can be omitted
- `@<ruby>{word,furigana}` : give furigana
- `@<fig>{tag}[caption](file)` : insert image
- `@<fig>(tag)` : figure reference
- `@<tbl>{tag}[caption]` ... `@<tbl>` : table block
- `@<tbl>(tag)` : table reference
- `@<list>{tag}[caption](file)` : insert code
- `@<list>{tag}[caption]` ... `@<list>` : literal code block
- `@<list>(tag)` : list reference
- `@<cmd>{option}` ... `@<cmd>` : command-line session
- `@<slabel>{tag}` ... label the section
- `@<sref>(tag)` ... reference to section

`@<fig>{`, `@<tbl>{` and `@<list>{` can take options at end
in `{...}` form: e.g., `@<line>{...}[...]{linenos=off}`

Do not add `#` in front of tags specified in `@<...>` commands;
they automatically add one if necessary.
