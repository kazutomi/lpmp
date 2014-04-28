# lpmp - Leanpub Markdown Preprocessor
--------

## Usage

    $ lpmp

The command reads Book.txt and *.lmp files
and generates corresponding .txt files.

## Commands available in .lmp files

- `@<kw>{word,yomi}` : keyword to be indexed; yomi can be omitted
- `@<ruby>{word,furigana}` : give furigana
- `@<fig>(#tag)` : figure reference
- `@<fig>{#tag}[caption](file)` : insert image
