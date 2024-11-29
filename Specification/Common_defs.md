# Common definitions

Comments start with `#`.

## Parts of entries

Name of a tag is case insensitive.

*References*

Each file may list references. Those are placeholders for parts which will repeat itself
such as names of verb persons, names of conjugations etc. The format for references are:

```
ref <name> <text>
```

To use a reference just place its name in the place of data. For example:

```
ref conj "coniugātiō īrregularis"

task 1 conjugate &conj &form "sum" "to be" &persons sum,es,est,sumus,estis,sunt
```

References should be first defined and then used and they apply only to that file. But the language
file shares all its references with other files.

References do not replace a part of data but the whole part. For example, in a part `"a &word"` the
`word` reference won't be replaced.

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
