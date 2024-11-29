# Common definitions

Comments start with `#`.

## Parts of entries

Name of a tag is case insensitive.

## Definitions

### `<text>`

Text part in definitions is expected to be a word or double-quoted sentence.

Examples:
```
Latin
2024.01.01.
"Do not use macros"
```

### `<id>`

Identifier part in definitions is expected to be a word which can be used as
reference in other places. It should contain only Lain alphabet letters,
underline and numbers.

Examples:
```
licence1
decl1
sg_f
```

### `<content>`

Content part in definitions is expected to be a markdown-enabled text of data.
It is expected to be text block marked with start-of-text (`<EOL`) and
end-of-text (`EOL`) markers.

### `<file-path>`

File path part in definitions is expected to be a path to a file. This path can
be relative but also URL.
