# Common definitions

This document describes common definitions in language source files.

## Comments

In source files comments begin with hashtag symbol (`#`) and ends at the end of
line.

## Entries

Source files consist of entries. Each entry has its tag and parts. Parts are separated by space. Multiple space characters are perceived as one.

Tag names are case insensitive.

For example:

```
ref ref1 "First reference"
```

Here `ref` is a tag part for reference entry. Parts `ref` and
`"First reference"` are other parts which depend of reference format which is:

```
ref <id> <text>
```

Common definitions are described in this document.

## Forced newline

When entries are too long forced newline can be used. It is slash symbol (`\`)
at the end of line. It specified that entry continues on the next line.

## Definitions

### `<id>`

Identifier part in definitions is expected to be a word which can be used as
reference in other places. It should contain only Lain alphabet letters,
numbers, underline and dash.

Examples:
```
licence1
decl1
sg_f
```

### `<text>`

Text part in definitions is expected to be a word or double-quoted sentence.
When displaying this data double-quotes will not be shown.

Examples:
```
Latin
2024.01.01.
"Do not use macros"
```

Double-quoted part is expected to be on the same line. Newline character (`\n`)
will be perceived as end-of-entry.

### `<content>`

Content part in definitions is expected to be a markdown-enabled text of data.
It can be `<text>` format part but also a text block marked with start-of-line
(`<EOL`) and end-of-line (`EOL`) markers.

Newline character inside block will not be perceived of end-of-entry. The tab
character (`\t`) or four spaces at the start of the line will be ignored.

After end-of-line marker entry continues on the same line.

Examples:
```
" - Test"
<EOL
    This is a block
    which can continue to multiple
    lines.
EOL
```

### `<file-path>`

File path part in definitions is expected to be a path to a file. This path can
be relative but also URL.

It is expected to be in same format as `<text>` part.

## Common tags

*References*

Each file may list references. Those are placeholders for parts which will
repeat itself such as names of verb persons, names of conjugations etc. The
format for references is:

```
ref <name> <text>
```

To use a reference just place its name in the place of data. For example:

```
ref conj "coniugātiō īrregularis"

task 1 conjugate &conj &form "sum" "to be" &persons sum,es,est,sumus,estis,sunt
```

References should be first defined and then used. They apply only to that file.
But the language file shares all its references with other files.

# Changes

11.02.2025. - Initial version
