# Repository of languages

This document describes structure of repository of languages.

## Structure

 - `Languages.txt` - main repository file

This is the main file of repository. It describes repository and lists
languages in it. Subdirectory to the specific language is pointed by `language`
tag. 

 - `<language>/Language.txt` - language file

This file describes language in repository. It lists lessons, theory, trainings
etc. Format of this file is described in [Language.md](Language.md)

 - `<language>/<lesson>.txt` - a lesson file

This file describes a lesson. The language file points to it with a `lesson`
tag. It contains theory of the lesson and tasks. Format of this file is
described in [Lesson.md](Lesson.md).

 - `<language>/<training>.txt` - a training file



 - `<language>/<theory>.txt` - a theory file

This file described a theory for specific language topic. The language file
points to it with a `theory` tag. It contains theory chapters. Format of this file is described in [Theory.md](Theory.md).

# Changes

11.02.2025. - Initial version
