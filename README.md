# Data structure

This file describes structure of data used by Sīc Locūtus application. For general information look
in a main readme file.

Author: Armands Arseniuss Skolmeisters

## Structure

The data files for certain language are assumed for be in one directory. The main file which
describes a language is "Language.txt". It contains configuration, shared information and pointers
to lessons, trainings and theory.

The data files consist of lines which should start with a keyword. Lines starting with a number
sign ('#') are ignored. Used lines are split into parts by whitespace. When a part requires a
whitespace in it, that part should be enclosed with quotation marks ('"').

There are specific rules and format for each keyword.

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

### Trainings

Trainings are collections of tasks within specific category for example "Irregular verbs". Each
training is in one file. References to a lesson should be listed in the language file.

### Theory

TODO: 1. for lessons
TODO: 2. small descriptions, explanations
TODO: 3. general chapters
TODO 3.1. both languages?

## Tasks

There are various tasks for user to do such as conjugate a verb, decline a noun etc. Each task has
its unique data.

All tasks are described in this format:

```
task <no> <type> ...
```
where
 - `no`: unique task number (or identifier) in that file,
 - `type`: task type.
 - `...`: more data depending of task type.

To identify specific task the system will use the name of the file and task number, e.g.:

Lesson1.txt:
```
task 1 ...
```

will be identified as `Lesson1.txt-1`.

### Casing task

The **casing task** is a task where the user have to select name of case. For example in "rosa
puellae" the noun "puella" is in genitive.

- Points: 1 per case

Task format:

```
task <no> casing <meaning> <sentence> <answer> <options>
```
where
 - `meaning` - TODO,
 - `sentence` is sentence to which casing should be given,
 - `answer` is case answer to words or skipped if that word do not need to be tested,
 - `options` are list of options.

For example:
```
task 1 casing "I have a red rose." "Rosam rūbrum habeō" Acc.,Acc., Nom.,Gen.,Dat.,Acc.,Abl.,Voc.
```

### Choose task

The **choose task** is a task where the user have to select correct answer.

- Points: 1

**TODO**: Count of how many options are shown

### Conjugate task

The **conjugate task** is a task where user have to conjugate a verb in specific form for specific
persons. The task gives user a verb, its meaning and a list of persons to conjugate it.

- Points: 1 per person

Task format:

```
task <no> conjugate <conjugation> <description> <verb> <meaning> <persons> <answers>
```
where
 - `conjugation`: verb conjugation,
 - `description`: verb form consisting of tense, voice and mood,
 - `verb`: verb (in form as could be seen in a dictionary),
 - `meaning`: translation of the verb to the main language,
 - `persons`: comma separated list of possible conjugation persons,
 - `answers`: comma separated list of correct answers.

Rule: If any of answers are not specified (empty), the user will not need to answer it.
Rule: The answers may contain alternative variants. Each variant is considered correct for user to
answer. In answers part the variants are separated by slash symbol ('/').

Note: The conjugation and description part is used to configure a custom training session. These
parts should be in the same format.

### Decline task

The **decline task** is a task where user have to decline a noun.

- Points: 1 per case
- Rule: Some answers may have '*' to show that they are just to be shown
- Given cases are in *decline* tag:

```
decline nōminātīvus genetīvus datīvus accūsātīvus ablātīvus vōcātīvus
```

The **degree task** is an task where user have to write comparable forms for two words in a certain
case.

The **guess task** is a task where user have ... TODO.

The **macron task** is a task where user have to write a text using correct macrons.

- Usage of macrons are enabled using *macron* tag:

```
macron on
```

The **number task** is a where where user have to write correct ordinal or cardinal number.

The **possess task** is a task where user have to write correct possive form.
TODO: same as choose.

The **translate task** is a task where user have to translate a certain sentence.
TODO: write in themself or choose from "bubbles"

TODO: Question task
TODO: Choose picture task
TODO: change to passive form
