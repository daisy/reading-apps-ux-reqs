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

[28 April 2025]{.pubdate}

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
  - [Visual Adjustments - Text](#visual-adjustments---text)
  - [Visual Adjustments - Images](#visual-adjustments---images)
  - [Visual Adjustments - Math](#visual-adjustments---math)
  - [Visual Adjustments - Color and Brightness](#visual-adjustments---color-and-brightness)
  - [Navigation](#navigation)
  - [Read Aloud](#read-aloud)
  - [Search](#search)
  - [Reading](#reading)
  - [Images](#images)
  - [Tables](#tables)
  - [Links and Footnotes](#links-and-footnotes)
  - [Mathematical Expressions](#mathematical-expressions)
  - [Notes and Highlights](#notes-and-highlights)
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

### Visual Adjustments - Text

User story: [Oxana](https://daisy.github.io/reading-apps-ux-reqs/use-cases/#oxana), 
[Ruth](https://daisy.github.io/reading-apps-ux-reqs/use-cases/#ruth),
[Alex](https://daisy.github.io/reading-apps-ux-reqs/use-cases/#alex),
[Stefan](https://daisy.github.io/reading-apps-ux-reqs/use-cases/#stefan),
[Javier](https://daisy.github.io/reading-apps-ux-reqs/use-cases/#javier)

#### The user must be able to change the typeface.

The user should be able to change the typeface of all text, choosing from a range including sans serif and serif fonts. Individuals with low vision or dyslexia often have specific preferences for font styles that optimize their reading experience. Typefaces with preferred letter shapes can aid in visual processing, improve comprehension and reduce cognitive load.

Priority: Must-have

Sources: [visual-010 : Change font](https://www.epubtest.org/test-books/visual-adjustments/2.0.0/visual-510), 
[Accessibility Requirements for People with Low Vision: font face](https://w3c.github.io/low-vision-a11y-tf/requirements.html#font)

#### The user must be able to change the font weight.

Visual readability of text requires good visual contrast. Visual contrast is a product of the text characteristics, such as font weight (thickness, font stroke width) and font size, the lightness/darkness difference of the colors used for the text and the background, and other factors. For some people, bold text is easier to read which is why they should be have bold font options. Many typefaces have a bold font and some offer variable weight. 

Priority: Must-have

Sources: [WCAG Accessibility Guidelines 3.0 - Draft version: visual contrast of text](https://www.w3.org/WAI/GL/WCAG3/2020/methods/font-characteristics-contrast/), [Accessibility Requirements for People with Low Vision: text style](https://w3c.github.io/low-vision-a11y-tf/requirements.html#style)

#### The user must be able to change the text size.

Some people need to increase the size of text in order to read it. Although increasing size is most common, some people with tunnel vision and good visual acuity may prefer to decrease the size so they can see more text at a time.

Priority: Must-have

Sources: [visual-010 : Change font size](https://www.epubtest.org/test-books/visual-adjustments/2.0.0/visual-010), 
[Accessibility Requirements for People with Low Vision: font size](https://w3c.github.io/low-vision-a11y-tf/requirements.html#text-size),
[The effect of print size on reading speed in dyslexia. Journal of Research in Reading](https://doi.org/10.1111/j.1467-9817.2005.00273.x)

#### The user should be able to remove the visual text styling (underline, italic, bold).

For some people, it is difficult to read text that is italicized, underlined or bold. Users should have the option to view the text without these visual formatting styles. However, underlining should be retained for hyperlinks. While removing formatting may result in the loss of some semantic significance, users should be able to toggle back to the visually formatted version as needed.

Priority: Should-have

Sources: [Accessibility Requirements for People with Low Vision: text style](https://w3c.github.io/low-vision-a11y-tf/requirements.html#style)

#### The user could be able change the capitalization of text to sentence style.

Text written in all capital letters or all small capital letters is more difficult to read for most people, with and without disabilities. Users should have the option to choose a sentence-style version. Acronyms that are correctly marked as abbreviations will remain in uppercase; otherwise, they will be converted to sentence style. Users should also be able to toggle between the different styles as needed.

Priority: Could-have

Sources: [Accessibility Requirements for People with Low Vision: capitalization](https://w3c.github.io/low-vision-a11y-tf/requirements.html#capitalization)

#### The user must be able change the line spacing, word spacing and letter spacing.

The amount of line spacing (leading), word spacing (space between words) and letter spacing (space between letters/characters) impacts readability. Some people need more space to read text and will have individual preferences. Line spacing also helps with tracking.

User story: [Ruth](https://daisy.github.io/reading-apps-ux-reqs/use-cases/#ruth),
[Javier](https://daisy.github.io/reading-apps-ux-reqs/use-cases/#javier)

Priority: Must-have

Sources: [Accessibility Requirements for People with Low Vision: line spacing](https://w3c.github.io/low-vision-a11y-tf/requirements.html),
[Extra-large letter spacing improves reading in dyslexia](https://doi.org/10.1073/pnas.1205566109).

#### The user must be able turn off justification and center-alignment of blocks of text.

Justification impacts readability and tracking. Fully justified text creates uneven spaces between words and letters, leading to "rivers of white space" that disrupt reading flow and visual tracking, particularly for people with dyslexia. Users with low vision who rely on screen magnifiers may encounter exaggerated gaps or overlapping characters in justified text, making it harder to read. Center-aligned text is also problematic for multi-line blocks, as it disrupts smooth reading flow and makes it harder to find the beginning of lines. Depending on the reading order of the language concerned (left to right, or right to left) turning the justification or center-alignment off results in a left-aligned or right-aligned text. 

Priority: Must-have

Sources: [Accessibility Requirements for People with Low Vision: justification/alignment](https://w3c.github.io/low-vision-a11y-tf/requirements.html#justification)

#### The user must be able to change the margins and adjust the line length for blocks of text.

Having wide margins results in shorter line lengths. This can be helpful for some people with specific learning disabilities. Having wide margins around blocks of text helps some people focus on the text and not get distracted by other content. 

Conversely, wide margins can make line length too short for people who use large text.

User story: [Oxana](https://daisy.github.io/reading-apps-ux-reqs/use-cases/#oxana)

Priority: Must-have

Sources: [Accessibility Requirements for People with Low Vision: margins and borders](https://w3c.github.io/low-vision-a11y-tf/requirements.html#margins-and-borders),
[Shorter Lines Facilitate Reading in Those Who Struggle](https://doi.org/10.1371/journal.pone.0071161)

#### The user must be able to view the content in a scrolling view.

For reflowable content, if the reader offers a paginated view, then the user should also be able to vie it in a scrollabe view.

User story: 

Priority: Must-have

Sources: 

#### The user could be able to view the content in a paginated view.

User story: [Ruth](https://daisy.github.io/reading-apps-ux-reqs/use-cases/#ruth)

Priority: Could-have

Sources: 

#### The user should be able to visually emphasize the text being read using a contrasting highlight, ruler lines, deemphasizing the surrounding text, or other means.

There are many ways this can be done. Here are some implementation examples: [...]

User story: [Alex](https://daisy.github.io/reading-apps-ux-reqs/use-cases/#alex)

Priority: Should-have

Source: [ReadAloud-610 : Text is emphasised as it is spoken by read aloud](https://www.epubtest.org/test-books/read-aloud/2.0.0/ReadAloud-610)

### Visual Adjustments - Images

#### The user must be able to enlarge images.

The user should be able to select an image and make it larger. There should be controls to adjust the size and to pan around an image when it no longer fits within the display.

A custom color theme used for viewing the text can sometimes render parts of the image difficult to see. There could be the option in the image viewer to revert to the default color mode, or to choose different color themes.

User story:

Priority: [Must-have]

Source: [visual-710 : Enlarge SVG Images](https://www.epubtest.org/test-books/visual-adjustments/2.0.0/visual-710)

### Visual Adjustments - Math

#### The user must be able to adjust the size and color of math expressions by adjusting the text's font size and color.

Math expressions included as MathML (or LaTeX, if supported) should be displayed correctly. As the user adjusts the size and colors of the text content, the math expressions should change accordingly. As the text size is increased, so should the math expressions in proportion. As the user changes the colors for the text content, this should also affect the math expressions.

User story:

Priority: Must-have

Source: [visual-550 : Viewing MathML](https://www.epubtest.org/test-books/visual-adjustments/2.0.0/visual-550)

#### The user should be able to enlarge math expressions for closer inspection.

Math expressions often contain small symbols such as exponents, indices, dot notations and derivatives. It should be possible for the user to view a math expression as a separate item and enlarge it.

Priority: Should-have

Source:

#### The user could be able [to flatten the colors of math expressions].

Certain parts of math expressions are sometimes presented in special colors, e.g. superscript in red. For some people this can present problems. The user could be able to remove the color formatting used in math expressions so the chosen text color is always used.

User story:

Priority: Could-have

Source:

### Visual Adjustments - Color and Brightness

#### The user must be able to personalize the background and foreground colors.

The user should be able to set the background and text color from the full color spectrum.

Some people need high contrast between text and background, including many older people who lose contrast sensitivity from ageing. Some read better with dark text on light background. Others find it easier to read with low contrast and colors that present less glare.

For some people, common color combinations or colors from a limited color palette work fine, for example, black text on white background or the inverse with white text on black background. For instance, black text on a white background is specifically useful for people with dyslexia. Other people need to select more specific background and text colors. For example, people who need low brightness overall, need to select the specific background and text colors that provide sufficient contrast for them yet not too high brightness. Readable and optimal color combinations differs vastly among individuals and can even vary for one individual depending on conditions such as fatigue and lighting.

User story:

Priority: [Must-have for a limited color palette; Should-have for more specific background and text colors]

Sources: [visual-110 : Change background and foreground color](https://www.epubtest.org/test-books/visual-adjustments/2.0.0/visual-110), [Accessibility Requirements for People with Low Vision: text contrast](https://w3c.github.io/low-vision-a11y-tf/requirements.html#text-contrast)

#### The user must be able to use the app with the high contrast and magnification features of the operating system platform.

Some people use high contrast modes on their device because it increases readability by maximizing the difference between text and background. Some people use the magnification feature of the operating system, or third party tools, to increase the size of text and images on the display.

Users must be able to use these features with the reading app. The app should respect the high contrast settings chosen by the user.

User story: [Stefan](https://daisy.github.io/reading-apps-ux-reqs/use-cases/#stefan)

Priority: Must-have

Source: [visual-310 : Apply high contrast system configuration](https://www.epubtest.org/test-books/visual-adjustments/2.0.0/visual-310)

#### The user must be able to change the display brightness.

Some individuals with low vision or dyslexia may have photophobia or light sensitivity. The ability to dim the screen can make reading more comfortable for these users. For some people with age-related macular degeneration, brighter illumination has been shown to improve reading acuity, critical print size, and maximum reading speed. Adjusting brightness can enhance the contrast between text and background, making it easier for individuals with low vision to distinguish letters and words.

The user must be able to adjust the display brightness when using the reading app. If this is not possible on the device or the operating system, it must be possible in the reading app itself.

If it is possible to adjust the display brightness on the device or in the operating system, it could be possible in the reading app itself.

Priority: Must-have

[visual-210 : Change brightness](https://www.epubtest.org/test-books/visual-adjustments/2.0.0/visual-210),
Legge G. E. (2016). Reading Digital with Low Vision. Visible language, 50(2), 102–125. (https://pmc.ncbi.nlm.nih.gov/articles/PMC5726769/)

### Navigation

#### The user must have a simple way to navigate the list of available publications and open a selected title.

User story: [Oxana](https://daisy.github.io/reading-apps-ux-reqs/use-cases/#oxana), [Louis](https://daisy.github.io/reading-apps-ux-reqs/use-cases/#louis)

Priority: Must-have

Source: [EPUBTest file-210 Open content](https://www.epubtest.org/test-books/basic-functionality/2.0.0/file-210)

#### The user must have a simple way to navigate forward and backward through the content.

For content with text it must be possible to move forward and backward from the currently displayed screen.

For content with audio it must be possible to move forward and backward using time-based navigation.

Priority: Must-have

Sources: [EPUBTest nav-210 Navigate forward and backward through reflowed content](https://www.epubtest.org/test-books/basic-functionality/2.0.0/nav-210), 
[EPUBTest nav-510 Move across chapters without using TOC](https://www.epubtest.org/test-books/basic-functionality/2.0.0/nav-510), 
[EPUBTest reading-1210 : Navigate the content by headings](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-1210),
[EPUBTest nav-110 Navigate content by pages](https://www.epubtest.org/test-books/basic-functionality/2.0.0/nav-110)

#### The user must have a way to navigate the publication using the Table of Contents.

The focus must be on the entry for the current reading position when the user is presented with the table of contents. If the publication's table of content comprises a hierachy of entries (eg volumes, chapters, subsections) then it must be presented as a tree view, nested list view or any other view that conveys the structure to the user. The user must have a mechanism to move between items in the table of contents of the same level (eg between the chapters without having to go via the subsections).

Page numbers or percentage information could be provided in the table of contents. The user could be able to search within the table of contents.

User story: [Maria](https://daisy.github.io/reading-apps-ux-reqs/use-cases/#maria), [Javier](https://daisy.github.io/reading-apps-ux-reqs/use-cases/#javier)

Priority: Must-have

Sources: [EPUBTest nav-010 Navigate to chapters through the Table of Contents](https://www.epubtest.org/test-books/basic-functionality/2.0.0/file-210), 
[EPUBTest nav-005 The table of contents in the app presents the content hierarchy](https://www.epubtest.org/test-books/basic-functionality/2.0.0/nav-005)

#### The user must have a way to navigate the content by pages.

When the publication includes page markup then it must be possible to navigate by page numbers. If the publication does not include page markup it could be possible to navigate by 'pseudo pages' (where the app uses an algorithm to approximate navigation points equivalent to typical page lengths).   

User story: [Maria](https://daisy.github.io/reading-apps-ux-reqs/use-cases/#maria), [Javier](https://daisy.github.io/reading-apps-ux-reqs/use-cases/#javier)

Priority: Must-have

Sources: [EPUBTest nav-010 Navigate to chapters through the Table of Contents](https://www.epubtest.org/test-books/basic-functionality/2.0.0/file-210), 
[EPUBTest nav-005 The table of contents in the app presents the content hierarchy](https://www.epubtest.org/test-books/basic-functionality/2.0.0/nav-005)

#### The user must have a way to go to a specific location in audio-based content.

When reading audio-based content it must be possible to go to a specific location. This could be based on time, percentage, or another approach.

Priority: Must-have

#### Screen reader/assistive technology users must be able to navigate through content by headings, block items, lines, words and characters.

User story: [Maria](https://daisy.github.io/reading-apps-ux-reqs/use-cases/#maria)

Priority: Must-have

Sources: [EPUBTest reading-810 : Move to the next block item](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-810),
[EPUBTest reading-1110 : Navigate by lines](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-1110),
[EPUBTest reading-1010 : Navigate by words](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-1110),
[EPUBTest reading-910 : Navigate by characters](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-910)

#### Screen reader/assistive technology users must be able to read continuously from the current position, and be able to pause, then resume reading from the paused reading location.

User story: [Alice](https://daisy.github.io/reading-apps-ux-reqs/use-cases/#alice), [Liviu](https://daisy.github.io/reading-apps-ux-reqs/use-cases/#liviu)

Priority: Must

Sources: [reading-010 : Initiate "read from here"](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-010),
["reading-110 : Stop and resume reading at the same reading location"](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-110)

#### The user must have a way to save their progression in the publication and return the user to the last location they saved the next time they open the publication.

When reading text-based content it must be possible to return to the approximate location (such as the same page or screen of text). It could be possible to return to the exact last location.

When reading audio-based content it must be possible to return to the exact last location.

Priority: Must-have

#### The user must be able to determine their location in the content.

The user must be able to get information about their current position in the book without losing their reading position. The minimum information expected is the percentage progress.

The user should be able to determine the current chapter, section, current page number where this information is provided in the publication.

Priority: Must-have

Source: [nav-310 Read navigation information](https://www.epubtest.org/test-books/basic-functionality/2.0.0/nav-310)

### Read Aloud

In this requirements document the term "read aloud" refers to the app using Text To Speech (TTS) to provide an audio option for text-based content.

#### The user must be able to listen to text-based content using synthetic speech (Text To Speech).

The user must be able to use a TTS read aloud feature for text-based content. If the publication also has synchronised audio with the text then the user must be able to choose the alternative of listening to the TTS read aloud.

Priority: Must-have

Source: [ReadAloud-010 : The content can be read aloud](https://www.epubtest.org/test-books/read-aloud/2.0.0/ReadAloud-010)

#### The user must be able to control the starting position of the read aloud.

The user should be able to choose the position from where the read aloud begins. 

If a screen reader is being used then the read aloud should start from the screen reader position.

If a screen reader is not being used then:

- If the user has indicated a start position then read aloud should start from there.
- If the user has made no selection, then read aloud should start from an approximate reading position (eg the first visible text on the display).

Priority: Must-have

#### The user must be able to read aloud selected parts of the content.

The user should be able to select text (e.g. word, phrase, sentence, paragraph) and have that read aloud.

Priority: Must-have

#### The user must be able to listen to the read aloud without having to manually advance to subsequent pages or chapters.

The read aloud must be able to read continuously until the end of the publication unless interupted by the user.

The read aloud could support a sleep function, pausing the read aloud after a user determined period of time.

Priority: Must-have

#### The user could be able to choose from a range of read aloud modes.

The user could be able to set the mode so that read aloud is not continuous. The amount read should be chosen by the user (eg read aloud stop after each word, sentence, paragraph, page or chapter). 

Priority: Could-have

#### The user must be able to have the content read aloud in the logical reading order.

Priority: Must-have

Source: [reading-210 : All text should be read in the proper order](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-210), 
[ReadAloud-310 : All text should be read in the proper order](https://www.epubtest.org/test-books/read-aloud/2.0.0/ReadAloud-310)

#### The user of read aloud must hear appropriate pauses after headings, paragraphs, list items, etc.

The read aloud must use appropriate pauses after headings, list items etc., rather than reading as if it is one continuous section of text. The read aloud implementation should pay attention to commonly used text content such as numbered heading and lists.

Priority: Must-have

Source: [EPUBTest reading-510 : TTS allows pause for indicating headings, paragraphs, list items, etc](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-510), 
[ReadAloud-510 : Text to Speech handles punctuation and document structure appropriately](https://www.epubtest.org/test-books/read-aloud/2.0.0/ReadAloud-510)

#### The user could be able to adjust read aloud to change the pause length between content blocks.

The user could be able to adjust the pauses between sentences, paragraphs, etc.

Priority: Could-have

#### The user must be able to view the text being read aloud.

The user must be able to view the text on the display as the read aloud position continues beyond the text initially visible.

The user could have the option for read aloud without text display (eg on the lock screen)

Priority: Must-have

#### The user must be able to visually emphasize the text being read aloud and be able to turn this feature off.

The user must be able to visually emphasize the text as it is read aloud using a contrasting highlight, underlining, or other means. Some users will be hindered by this visual cue, e.g. due to health concerns such as epilepsy. Overly granular, like word-by-word highlighting could also be distracting.

The user must be able to to turn off the read aloud visual emphasis.

Priority: Must-have

Source: [ReadAloud-610 : Text is emphasised as it is spoken by read aloud](https://www.epubtest.org/test-books/read-aloud/2.0.0/ReadAloud-610)

#### The user must be able to change the color or style of the visual emphasis.

The user must be able to adjust the visual emphasis.

The user could be able to adjust the number of words that are highlighted at any time.

Priority: Should-have [or Could-have]

Source: [ReadAloud-610 : Text is emphasised as it is spoken by read aloud](https://www.epubtest.org/test-books/read-aloud/2.0.0/ReadAloud-610)

#### The user of read aloud must hear content in the correct language.

The user must be able to hear the read aloud using the correct voice when reading content with language tags (if available to the reading app). The user should be able to override language switching and select the language to be used for all content.

The read aloud could switch between dialects of the same language. If this feature is supported the user must be able to disable it.

Priority: Must-have

Source: [reading-1510 : TTS Change Languages Automatically](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-1510)

User Story: [Louis](https://daisy.github.io/reading-apps-ux-reqs/use-cases/#louis)

#### The user must be able to control the voice and speed of the read aloud.

The user must be able to select from a range of voices. The user must be able to choose the speed of the read aloud voice.

The reading app should not distort the pitch when the user has selected higher listening speeds.

Priority: Must-have

Source: [ReadAloud-400 : Change Read Aloud reading voice](https://www.epubtest.org/test-books/read-aloud/2.0.0/ReadAloud-400)

#### The user must be able to listen to image alt text.

The read aloud feature must be able to announce the alt text of images. 

The user must be able to turn off the read aloud of image alt text. The user should be able to escape from the image alt text once the read aloud has started.

The image alt text could be distinguished from text content with an announcement, use of different voice, or other technique.

Priority: Must-have

#### The user could be able to choose to have semantic expressiveness for read aloud.

The user could be able to adjust the pitch or style for emphasized text (eg bold, italic, underlined). If this feature is supported the user must be able to disable it.

Priority: Could-have

#### The user must be able to listen to math content when using read aloud.

The read aloud feature must be able to announce encoded math content (eg MathML).

The user should be able to adjust the announcement of math content according to their preference (eg relative reading speed,  reading style, verbosity).

Priority: Must-have

#### The user must/should/could be able to use read aloud with tables

What should the experience be?

Skippability/escapability?

Priority level?

#### The user should be able to decide to skip read aloud of anciallary content 

Ancillary content includes aside, bibliography, endnotes, footnote, noteref, pullquote.

Priority: Should-have

#### The user should be able to decide to skip read aloud of navigation content 

Navigation content includes landmarks, lists of audios, tables, images or videos, pagebreak and table of contents.

Priority: Should-have

#### The user must/should/could be able to use read aloud with footnotes and endnotes

What should the experience be?

Skippability/escapability?

Priority level?

#### The user must/should/could be able to use read aloud with expandable/collapsable content

What should the experience be?

Skippability/escapability?

Priority level?

### Search

#### The user must be able to perform a search and review the search results.

Priority: Must-have

Source: [nav-410 : Perform a search, review the search results](https://www.epubtest.org/test-books/basic-functionality/2.0.0/nav-410)

### Reading

#### The user must be able to read through content in the logical reading order.

Priority: Must-have

Source: [reading-210 : All text should be read in the proper order](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-210), 
[ReadAloud-310 : All text should be read in the proper order](https://www.epubtest.org/test-books/read-aloud/2.0.0/ReadAloud-310)

#### Screen reader/assistive technology users should hear appropriate pauses after headings, paragraphs, list items, etc.

Priority: Must-have

Source: [EPUBTest reading-510 : TTS allows pause for indicating headings, paragraphs, list items, etc](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-510), 
[ReadAloud-510 : Text to Speech handles punctuation and document structure appropriately](https://www.epubtest.org/test-books/read-aloud/2.0.0/ReadAloud-510)

#### Screen reader/assistive technology users must be able to adjust the voice and reading speed.

Priority: Must-have

User Story: [Simona](https://daisy.github.io/reading-apps-ux-reqs/use-cases/#simona), [Javier](https://daisy.github.io/reading-apps-ux-reqs/use-cases/#javier)

Sources: [ReadAloud-400 : Change Read Aloud reading voice](https://www.epubtest.org/test-books/read-aloud/2.0.0/ReadAloud-400), 
[ReadAloud-410 : Change Read Aloud reading speed](https://www.epubtest.org/test-books/read-aloud/2.0.0/ReadAloud-410)

#### Screen reader/assistive technology users must be able to read content in the correct language (audio or braille).

Priority: Must-have

Source: [reading-1510 : TTS Change Languages Automatically](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-1510)

User Story: [Louis](https://daisy.github.io/reading-apps-ux-reqs/use-cases/#louis)

### Images

#### Screen reader users must be able to read and navigate within image descriptions.

Priority: Must-have

User Story: [Simona](https://daisy.github.io/reading-apps-ux-reqs/use-cases/#simona)

Source: [reading-310 : Image alternate text reading](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-310)

#### Read aloud users must have the option to hear image descriptions.

Priority: Must-have

Source: [ReadAloud-350 : Image alternate text reading](https://www.epubtest.org/test-books/read-aloud/2.0.0/ReadAloud-350)

### Tables

#### Screen reader/assistive technology users must be able to navigate between the cells, rows and columns in a table

Priority: Must-have

Source: [reading-610 : Navigate between the cells, rows and columns in the table](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-610)

### Links and Footnotes

#### Users must be able to navigate between internal hyperlinks.

Priority: Must-have

Source: [reading-710 : Navigate between internal hyperlinks](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-710)

#### Users must be able to detect the reference to a footnote, reach the content of the footnote, read the content of the footnote and provide a mechanism to move back to the original reading position from the footnote.

Priority: Must-have

Source: [reading-420 : Footnote Reading](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-420)

### Mathematical Expressions

#### The user must be able to read and navigate within mathematical expressions.

[Notes for editors: - The user should be able to explore mathematical expressions that are included as MathML or LaTeX. This is not expected if math is included as images.]

Priority: Must-have

User Story: [Louis](https://daisy.github.io/reading-apps-ux-reqs/use-cases/#louis)

Source: [EPUBTest reading-1410 : MathML Reading](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-210)

### Notes and Highlights

#### The user should be able to add, review and edit highlights.

Sources: [EPUBTest anno-010 : Add a Bookmark or Highlight](https://www.epubtest.org/test-books/basic-functionality/2.0.0/anno-010), 
[EPUBTest anno-110 : Review and navigate Bookmarks or Highlights](https://www.epubtest.org/test-books/basic-functionality/2.0.0/anno-110)

#### The user should be able to add, review and edit notes.

Sources: [EPUBTest anno-210 : Add a note](https://www.epubtest.org/test-books/basic-functionality/2.0.0/anno-210),
[EPUBTest anno-310 : Review and navigate Notes](https://www.epubtest.org/test-books/basic-functionality/2.0.0/anno-310)

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
