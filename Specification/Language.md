# Language file

Language file is main file describing a language. It contains primary
information about language, references and pointers to lessons, trainings and
theory.

References declared here can used in all other places: lessons, training
and theory.

## File specific tags

### `name` tag

Definition:
```
name <text>
```

This tag indicates name of language used in various places. It is just a name of 
language in display language. There can only be one name tag in language file.

### `version` tag

Definition:
```
version <text>
```

This tag indicates version of current edition. It is used in update process to
check if newer version is available. Version text of being compared as text.
There can only be one version tag in language file.

### `author` tag

Definition:
```
author <text>
```

This tag indicates author of language content.

### `license` tag

Definition:
```
license <id> <content> 
```

This tag indicates copyright of language content used. Content part of this tag
will be shown in "Licenses" section in application. This tag can be declared
multiple times for each part of content. It is expected to have all licenses and
copyrights listed.

### `setting` tag

Definition:
```
setting <id> <text> <type> <value>

<type> ::= boolean

<value> ::= <boolean-value>

<boolean-value> ::= true | false
```

This tag declares language specific setting.

// TODO

### `gen` tag

Generate tag is described in Generators.md file.

### `theory` tag

Definition:
```
theory <file-path>
```

This tag indicates location of one of theory segments shown in "Theory"
section in application. Theory file is described in Theory.md file.

### `lesson` tag

Definition:
```
lesson <file-path>
```

This tag indicates location of one of lesson chapters shown in "Lessons"
section in application. Lesson file is described in Lesson.md file.

### `training` tag

Definition:
```
training <file-path>
```

This tag indicates location of one of training chapters shown in "Trainings"
section in application. Training file is described in Training.md file.

# Changes

11.02.2025. - Initial version
