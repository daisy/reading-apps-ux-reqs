---
title:  'Reading Apps User Requirements'
author:
- Kirsten de Haan
- Richard Orme
keywords: [DAISY, Dedicon, accessibility, reading apps]
...

<!-- convert this document to HTML with pandoc user-reqs.md -f markdown -o index.html --strip-comments --css="../../common/styles.css" --css="user-reqs.css" -->
<!-- The DOCTYPE delaration at the top of the generated file then needs to be added  -->

<html xmlns="http://www.w3.org/1999/xhtml" lang="en" xml:lang="en">
<head>
<meta charset="utf-8">
<title>DAISY Reading Apps User Requirements</title>
<link rel="stylesheet" type="text/css" href="../../common/styles.css">
<link rel="stylesheet" type="text/css" href="user-reqs.css">
</head>
<body>
<header>
[![DAISY Consortium](https://daisy.org/wp-content/uploads/2019/04/daisy_high.jpg){.logo height=15%}](https://daisy.org)

<hgroup>

# DAISY Reading Apps User Requirements {.title}
[Working Draft]{.subtitle}

</hgroup>

[19 February 2025]{.pubdate}

Editors:

- [Kirsten de Haan](mailto:KirstendeHaan@dedicon.nl)
- [Richard Orme](mailto:rorme@daisy.org)

:::{.history}
[Document History]{.history-title}

- [Changes to this document](https://github.com/daisy/reading-apps-ux-reqs/issues?q=is%3Aissue+is%3Aclosed)
- [Report an issue](https://github.com/daisy/reading-apps-ux-reqs/issues)

:::
:::{.legalnotice}
Copyright © 2025 DAISY Consortium
:::
</header>
<nav>

## Table of Contents

- [Table of Contents](#table-of-contents)
- [Introduction](#introduction)
- [User Stories](#user-stories)
- [User Requirements](#user-requirements)
  - [Navigation](#navigation)
  - [Search](#search)
  - [Reading](#reading)
  - [Images](#images)
  - [Tables](#tables)
  - [Links and Footnotes](#links-and-footnotes)
  - [Mathematical Expressions](#mathematical-expressions)
  - [Notes and Highlights](#notes-and-highlights)
  - [Visual Adjustments](#visual-adjustments)
  - [Read Aloud](#read-aloud)
- [Acknowledgements](#acknowledgements)
- [References](#references)

</nav>

::: {#introduction .section}

## Introduction

This document is the main output of the [DAISY project to develop user requirements for reading apps](https://daisy.org/activities/projects/reading-apps-user-requirements/). The project draws on the collective expertise and experiences of [DAISY Consortium members and friends](https://daisy.org/about-us/membership/) to express user requirements of individuals with diverse print disabilities for reading digital publications.

This unique document is intended to inform developers and purchasers of specialized reading systems and provide inspiration for mainstream reading solutions.

:::
::: {#userstories .section}

## User Stories

The [user stories](https://daisy.github.io/reading-apps-ux-reqs/use-cases/) referenced in this document were developed by the working group.
:::
::: {#userrequirements .section}

## User Requirements

### Navigation

#### The user should have a simple way to navigate the list of available content and open a selected title.

User story: [Oxana](https://daisy.github.io/reading-apps-ux-reqs/use-cases/#oxana)

Source: [EPUBTest file-210 Open content](https://www.epubtest.org/test-books/basic-functionality/2.0.0/file-210)

#### The user should have a way to navigate the content through the Table of Contents or by pages.

User story: [Javier](https://daisy.github.io/reading-apps-ux-reqs/use-cases/#javier)

Sources: [EPUBTest nav-010 Navigate to chapters through the Table of Contents](https://www.epubtest.org/test-books/basic-functionality/2.0.0/file-210), 
[EPUBTest nav-005 The table of contents in the app presents the content hierarchy](https://www.epubtest.org/test-books/basic-functionality/2.0.0/nav-005)

#### The user should have a simple way to navigate content forward and backward by chapters, headings, pages, paragraphs.

Sources: [EPUBTest nav-210 Navigate forward and backward through reflowed content](https://www.epubtest.org/test-books/basic-functionality/2.0.0/nav-210), 
[EPUBTest nav-510 Move across chapters without using TOC](https://www.epubtest.org/test-books/basic-functionality/2.0.0/nav-510), 
[EPUBTest reading-1210 : Navigate the content by headings](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-1210),
[EPUBTest nav-110 Navigate content by pages](https://www.epubtest.org/test-books/basic-functionality/2.0.0/nav-110)

#### Screen reader/assistive technology users should be able to navigate through content by headings, block items, lines, words and characters.

Sources: [EPUBTest reading-810 : Move to the next block item](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-810),
[EPUBTest reading-1110 : Navigate by lines](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-1110),
[EPUBTest reading-1010 : Navigate by words](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-1110),
[EPUBTest reading-910 : Navigate by characters](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-910)


#### The user should be able to read continuously from the current position, and be able to pause, then resume reading from the paused reading location.

Sources: [reading-010 : Initiate "read from here"](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-010),
["reading-110 : Stop and resume reading at the same reading location"](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-110)

#### The user should have a way to save their progression in the publication and return the user to the last location they saved the next time they open the publication.

Source: [ReadAloud-110 : Stop and resume reading](https://www.epubtest.org/test-books/read-aloud/2.0.0/ReadAloud-110)

#### The user should be able to determine their location in the content.

The user should be able to get information about their current position in the book. The minimum information expected is current chapter/section and, 
if appropriate, current page number. Percentage or time read, time remaining, book title, author etc. can be additional useful information. 
It should be possible to resume reading from the last read position after using this command.

Source: [nav-310 Read navigation information](https://www.epubtest.org/test-books/basic-functionality/2.0.0/nav-310)

### Search

#### The user should be able to perform a search and review the search results.

Source: [nav-410 : Perform a search, review the search results](https://www.epubtest.org/test-books/basic-functionality/2.0.0/nav-410)

### Reading

#### Screen reader/assistive technology users should be able to read through content in the logical reading order.

Source: [reading-210 : All text should be read in the proper order](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-210), 
[ReadAloud-310 : All text should be read in the proper order](https://www.epubtest.org/test-books/read-aloud/2.0.0/ReadAloud-310)

#### Users of screen reader/assistive technology audio should hear appropriate pauses after headings, paragraphs, list items, etc.

Source: [EPUBTest reading-510 : TTS allows pause for indicating headings, paragraphs, list items, etc](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-510), 
[ReadAloud-510 : Text to Speech handles punctuation and document structure appropriately](https://www.epubtest.org/test-books/read-aloud/2.0.0/ReadAloud-510)

#### Screen reader/assistive technology users should be able to adjust the voice and reading speed.

Sources: [ReadAloud-400 : Change Read Aloud reading voice](https://www.epubtest.org/test-books/read-aloud/2.0.0/ReadAloud-400), 
[ReadAloud-410 : Change Read Aloud reading speed](https://www.epubtest.org/test-books/read-aloud/2.0.0/ReadAloud-410)

#### Screen reader/assistive technology users should be able to read content in the correct language (audio or braille).

Source: [reading-1510 : TTS Change Languages Automatically](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-1510)

### Images

#### Screen reader users should be able to read and navigate within image descriptions.

Source: [reading-310 : Image alternate text reading](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-310)

#### Read aloud users should have the option to hear image descriptions.

Source: [ReadAloud-350 : Image alternate text reading](https://www.epubtest.org/test-books/read-aloud/2.0.0/ReadAloud-350)

#### The user should have the possibility of enlarging images.

Source: [visual-710 : Enlarge SVG Images](https://www.epubtest.org/test-books/visual-adjustments/2.0.0/visual-710)

### Tables

#### Screen reader/assistive technology users should be able to navigate between the cells, rows and columns in a table

Source: [reading-610 : Navigate between the cells, rows and columns in the table](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-610)

### Links and Footnotes

#### Users should be able to navigate between internal hyperlinks.

Source: [reading-710 : Navigate between internal hyperlinks](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-710)

#### Users should be able to detect the reference to a footnote, reach the content of the footnote, read the content of the footnote and provide a mechanism to move back to the original reading position from the footnote.

Source: [reading-420 : Footnote Reading](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-420)

### Mathematical Expressions

#### Screen reader users should be able to read and navigate within mathematical expressions.

Source: [EPUBTest reading-1410 : MathML Reading](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-210)

#### The user should be able to adjust the size and color of math expressions

Math expressions included as inline or block MathML should be displayed correctly. As the user adjusts the size and colors of the text content, the math expressions should change accordingly.

Source: [visual-550 : Viewing MathML](https://www.epubtest.org/test-books/visual-adjustments/2.0.0/visual-550)

### Notes and Highlights

#### The user should be able to add, review and edit highlights.

Sources: [EPUBTest anno-010 : Add a Bookmark or Highlight](https://www.epubtest.org/test-books/basic-functionality/2.0.0/anno-010), 
[EPUBTest anno-110 : Review and navigate Bookmarks or Highlights](https://www.epubtest.org/test-books/basic-functionality/2.0.0/anno-110)

#### The user should be able to add, review and edit notes.

Sources: [EPUBTest anno-210 : Add a note](https://www.epubtest.org/test-books/basic-functionality/2.0.0/anno-210),
[EPUBTest anno-310 : Review and navigate Notes](https://www.epubtest.org/test-books/basic-functionality/2.0.0/anno-310)

### Visual Adjustments

#### The user should have the possibility of personalizing the visual reading experience, controlling font size, choice of fonts, background and foreground color, and brightness.

Sources: [visual-010 : Change font size](https://www.epubtest.org/test-books/visual-adjustments/2.0.0/visual-010), 
[visual-110 : Change background and foreground color](https://www.epubtest.org/test-books/visual-adjustments/2.0.0/visual-110), 
[visual-210 : Change brightness](https://www.epubtest.org/test-books/visual-adjustments/2.0.0/visual-210)

#### The user should be able to use the app with the high contrast and magnification features of the operating system platform.

Source: [visual-310 : Apply high contrast system configuration](https://www.epubtest.org/test-books/visual-adjustments/2.0.0/visual-310)

### Read Aloud

Source: [ReadAloud-400 : Change Read Aloud reading voice](https://www.epubtest.org/test-books/read-aloud/2.0.0/ReadAloud-400)

#### The user should be able to visually emphasize the text being read using a contrasting highlight, ruler lines, deemphasizing the surrounding text, or other means.

Source: [ReadAloud-610 : Text is emphasised as it is spoken by read aloud](https://www.epubtest.org/test-books/read-aloud/2.0.0/ReadAloud-610)

#### Read aloud users should be able to control the starting position.

Source: [ReadAloud-010 : The content can be read aloud](https://www.epubtest.org/test-books/read-aloud/2.0.0/ReadAloud-010)

:::
::: {#acknowledgments .section}

## Acknowledgements

This project would not have been possible without the contributions of the DAISY members and Friends who participated in the project. Their valuable insights, expertise, and experiences have been instrumental in ensuring that the requirments capture a broad range of user needs.

This work is financially supported by [Dedicon](https://dedicon.nl).

:::
::: {#references .section}

## References

The [EPUB test: Latest test books](https://www.epubtest.org/test-books)
has many well-established fundamental accessibility tests which were extracted and adapted for this document.
The titles are:

1. [Fundamental Accessibility Tests: Basic
    Functionality](https://www.epubtest.org/test-books/basic-functionality)
1. [Fundamental Accessibility Tests: Non-Visual
    Reading](https://www.epubtest.org/test-books/non-visual-reading).
1. [Fundamental Accessibility Tests: Visual
    Adjustments](https://www.epubtest.org/test-books/visual-adjustments)
1. [Fundamental Accessibility Tests: Read
    Aloud](https://www.epubtest.org/test-books/read-aloud)

:::

</body>
</html>
