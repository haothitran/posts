---
layout: post
title: Taking and Organizing Lecture Notes
date: 2017-01-29
---

It took years for me to figure out what note-taking system worked best for me to comprehend and retain information. After experimenting with different methods each school semester, I have developed a system that worked for me:

1. Before lecture, read associated non-lecture materials.
2. During lecture, take notes by hand.
3. Afterwards, cherry pick information and examples from readings related to the actual lecture content.
4. Type up lectures notes and reading notes.
5. Organize digital notes into small sections.
6. Study only from personal notes.

## Handwriting Lecture Notes

While studying for my bachelors, it was interesting to observe the changes in the way other students took their notes. In my first year, students who took notes with their laptop far outnumbered those who took notes by hand. Now, in my last year, it has reversed. Like my peers, I've made the same transition from laptop to pen and paper.

I like the freedom that handwriting notes gives me. There are large blank spaces between sub-topics because who knows if the professor will re-visit them. There are arrows connecting various threads of ideas and concepts. Interspersed are shorthand notations of key terms and phrases I develop on the fly to keep up with the pace set by my professors. My notes are always a mess at the end of a lecture.

## Transcribing Notes

Most documents that students work with contain only text. Yet, when I look across the lecture hall from the last row, students with laptops or tablets are using a word processor. I think this tool is overkill for just taking notes. A plain text editor would accomplish the same task with less headaches involved because it is:

- Portable.
  - Multi-platform support.
- Simple.
  - Focus on content instead of formatting text.
  - [Markdown](https://daringfireball.net/projects/markdown/) syntax can provide structure.
- Searchable.
  - Able to search for keywords across directories and in individual files.

However, it is also essential to keep in mind its constraints:

- Non-linear thinking is better using a mind-map.
- Little support beyond basic mathematical equations.
- Creating complex tables is a chore.
- No support for tabular data.
- No support for graphs.

Thankfully, as most of my courses are in the social science, using plain text is more than enough for my needs. For my statistical courses, I default to entirely using handwritten notes because it is faster to write equations and calculations by hand.

### Using Text Editors

I’m a keyboard user. I like using keyboard shortcuts for regular tasks. Unfortunately, default notepad programs in majority of operating systems lack support for complex keyboard functions. Nor do they support folder view which is essential for my workflow. There are also a number of other features that I like:

- Keyboard navigation and function shortcuts.
- View folder structure and files in tree view.
- Automatically indent bullet points.
- Support for syntax highlighting.
- Customization (themes, syntax colouring, extensions).

As such, I use text editors for taking and organizing my school notes over notepad apps and traditional word processors.

## Organizing Folder Structure

Here is how I organize my courses and individual lecture notes into folders. By using `_` before the course code, I can ensure that my current semester’s courses remain at the top of the list for quick and easy accessibility. When the semester is over, I remove the `_` from current course folders for next semester’s round of courses.

```
school-notes/
├── _CRM102-introduction-to-criminology/
├─┬ _SOC483-advanced-statistical-nodeling/
│ ├── 00-course-outline
│ ├── 01-introduction
│ ├── 02-review-cross-tabulations-and-ANOVA
│ ├── 03-review-bivariate-correlation-and-regression
│ ├── 04-dummy-variable-coding
│ ├── 05-control-variables-and-block-loading
│ └── ...
├── HIS106-warfare-technology-and-social-change/
├── PHL333-philosophy-of-human-nature/
├── POL100-people-power-and-politics/
├── SOC105-introduction-to-sociology/
├── SOC473-classical-sociology-theory/
├── SOC475-contemporary-sociological-theory/
└── ...
```

## Conclusion

I believe that note-taking is a personal skill that you have to develop for yourself. My system here certainly does not work for everyone, especially for students who frequently work with non-text material. This doesn't mean that inspiration cannot be taken from learning from other people which is why I wrote this post. I've taken inspiration from various random people document their workflow, and wanted to contribute to the conversation in the event that someone found inspiration from mine.
