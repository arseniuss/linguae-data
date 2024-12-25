# Tasks

Tasks are main part of application. There are various tasks for user to do
such as conjugate a verb, decline a noun etc. Each task has its unique data.

All tasks are described in this format:
```
task <id> <type> ...
```
where
 - `id`: unique task identifier in that file,
 - `type`: task type,
 - `...`: more data depending on task type.

To identify specific task the system will use the name of the file and task identifier, e.g.:

Lesson1.txt
```
task 1 ...
```
will be identified as `Lesson.txt-1`.

## `casing` task

Casing task is a task where the user have to select name of correct case. For example in "rosa puellae" the noun "puella" is in genitive.

 - Points: 1 per case

Task format:
```
task <id> casing <meaning> <sentence> <answer> <options>
```
where
 - `meaning`: TODO,
 - `sentence`: sentence to which casing should be given,
 - `answer`: case answers to words or skipped if that word do not need to be tested,
 - `options`: list of options.

For example:
```
task 1 casing "I have a red rose." "Rosam rūbrum habeō" Acc.,Acc., Nom.,Gen.,Dat.,Acc.,Abl.,Voc.
```

## `choose` task

Choose task is a task where the user have to select correct answer.

 - Points: 1

Task format:
```
task <id> choose <description> <word> <answer> <additionals>
```
where
 - `description`: title of choose task (what to do) in display language,
 - `word`: word which is being checked,
 - `answer`: correct answer,
 - `additionals`: other possible answers (incorrect ones).

## `conjugate` task

Conjugate task is a task where user have to conjugate a verb in specific form
for specific persons. The task gives user a verb, its meaning and a list of
persons to conjugate it.

 - Points: 1 per person

Task format:
```
task <id> conjugate <conjugation> <description> <verb> <meaning> <persons> <answers>
```
where
 - `conjugation`: verb conjugation,
 - `description`: verb form consisting of tense, voice and mood,
 - `verb`: verb (in form as could be seen in dictionary),
 - `meaning`: translation of the verb to the display language,
 - `persons`: comma separated list of possible conjugation persons,
 - `answers`: comma separated list of correct answers.

Rule: If any of answer is not specified (empty), the user will not need to
answer it.
Rule: The answers may contain alternative variants. Each variant is considered
correct for user to answer. In answers part the variants are separated by slash
symbol ('/').

Note: The conjugation and description part is used to configure a custom
training session. These parts should be in the same format.

## `decline` task

Decline task is a task where the user have to decline a noun.

 - Points: 1 per case

Task format:
```
task <id> decline <declination> <description> <noun> <meaning> <cases> <answers>
```
where
 - `declination`: noun declination,
 - `description`: noun form consisting of number ans gender,
 - `noun`: noun (in a form as could be seen in disctionary),
 - `meaning`: translation of the noun to the display language,
 - `cases`: comma separated list of possible noun cases,
 - `answers`: comma separated list of correct answers.

Rule: If any of answer is not specified (empty), the user will not need to
answer it.
Rule: The answers may contain alternative variants. Each variant is considered
correct for user to answer. In answers part the variants are separated by slash
symbol ('/').

Note: The declination and description part is used to configure a custom
training session. These parts should be in the same format.

## `macron` task

Macron task is a task where the user have to put macrons.

 - Points: 1 per word

Task format:
```
```

## `number` task

Number task is a task where the user have to write out number given.

 - Points: 1 per word

Task format:
```
```

## `translate` task

Translate task is a task where the user have to write translation of a sentence.

- Points: 1 per word

Task format:
```
task <id> translate <sentence> <translation> <additionals>
```
where

// TODO
