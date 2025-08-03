# Lesson file

Lesson file describes a lesson. It is a collection of tasks with theory and
theme. Each lesson is in one file.

References declared in lesson file are applicable only to that lesson file.

Lesson gets included in application only if reference to lesson file is
referenced in language file.

## File specific tags

### `name` tag

Definition:
```
name <text>
```

This tag indicates the title of a lesson.

### `section` tag

Definition:
```
section <text>
```

This tag indicates section of a lesson.

### `description` tag

Definition:
```
description <content>
```

This tag describes content of a lesson.

### `chapter` tag

Definition:
```
chapter <id> <display-content> <language-content>
```
where
 - `id `: unique chapter identifier in that file,
 - `display-content`: markdown-enabled content of theory (in display language,
        English),
 - `language-content`: markdown-enabled content of theory (in target language).

This tag defines theory explaining the lesson.

### `task-ref` tag

Definition:
```
task-ref <id> <additionals>
```
where
 - `id`: pointer to task full identifier including,
 - `additionals`: additional information for the task. For example: in
    choosing task it will be other options.

Task reference tag is described in Tasks.md file.

### `task` tag

Task tag is described in Tasks.md file.

# Changes

11.02.2025. - Initial version
