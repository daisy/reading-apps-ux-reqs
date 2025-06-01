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
[Public Working Draft]{.subtitle}

</hgroup>

[1 June 2025]{.pubdate}

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
- [User Requirements](#user-requirements)
  - [Navigation](#navigation)
  - [Screen Reader Support](#screen-reader-support)
  - [Read Aloud](#read-aloud)
  - [Visual Adjustments](#visual-adjustments)
  - [Making Notes](#making-notes)
  - [TODO: Entering Answers](#todo-entering-answers)
  - [TODO: Switching Modalities](#todo-switching-modalities)
  - [TODO: Library and Bookshelf](#todo-library-and-bookshelf)
- [User Stories](#user-stories)
- [Acknowledgements](#acknowledgements)
- [References](#references)
  

</nav>

::: {#introduction .section}

## Introduction

This document presents a comprehensive set of user requirements developed as part of the [DAISY project to develop user requirements for reading apps](https://daisy.org/activities/projects/reading-apps-user-requirements/). Its purpose is to help developers, designers, and decision-makers understand what individuals with diverse print disabilities need and expect from digital reading solutions- especially when it comes to accessibility, usability, and inclusive design.

Created through close collaboration between [DAISY Consortium members and friends](https://daisy.org/about-us/membership/), (DAISY Consortium members, accessibility experts, and developers of specialized reading apps), this resource captures a wide range of expert knowledge and practical insights. The document draws on the lived experiences of people with print disabilities and the requirements have been shaped and articulated by professionals with deep expertise in accessible reading technology.

This **public working draft** represents the results of the work carried out in the first part of the project. It is not yet comprehensive: several important topics still need to be addressed and will be added in future iterations. Feedback and collaboration are welcomed as the document evolves.

While the document is particularly relevant for those developing or procuring specialized reading apps, it also offers valuable guidance for those working on mainstream reading platforms who wish to make their products outstandingly accessible and user-friendly for everyone. Whether you're building a new reading application from the ground up or enhancing an existing one, we invite you to explore these requirements not just as a checklist, but as a roadmap toward more inclusive digital reading experiences.

:::
::: {#userrequirements .section}

## User Requirements

### Navigation

Effective navigation is a critical aspect of digital accessibility, particularly for users with diverse print disabilities. Users often face challenges in understanding where they are within a digital publication or application and how to move seamlessly between sections. Clear navigation structures, well-defined headings, and consistent cues are essential to help users orient themselves and access content efficiently. Screen reader users, who experience content in a linear format that is presented either as synthetic speech or via a braille display, depend heavily on these elements to avoid confusion and maintain a sense of control. Understanding and addressing these user requirements is key to creating inclusive digital experiences that empower all users to navigate content independently and with ease.

#### The user must have a simple way to navigate the list of available publications and open a selected title.

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

Priority: Must-have

Sources: [EPUBTest nav-010 Navigate to chapters through the Table of Contents](https://www.epubtest.org/test-books/basic-functionality/2.0.0/file-210), 
[EPUBTest nav-005 The table of contents in the app presents the content hierarchy](https://www.epubtest.org/test-books/basic-functionality/2.0.0/nav-005)

#### The user must have a way to navigate the content by pages.

When the publication includes page markup then it must be possible to navigate by page numbers. If the publication does not include page markup it could be possible to navigate by 'pseudo pages' (where the app uses an algorithm to approximate navigation points equivalent to typical page lengths).   

Priority: Must-have

Sources: [EPUBTest nav-010 Navigate to chapters through the Table of Contents](https://www.epubtest.org/test-books/basic-functionality/2.0.0/file-210), 
[EPUBTest nav-005 The table of contents in the app presents the content hierarchy](https://www.epubtest.org/test-books/basic-functionality/2.0.0/nav-005)

#### The user must have a way to go to a specific location in audio-based content.

When reading audio-based content it must be possible to go to a specific location. This could be based on time, percentage, or another approach.

Priority: Must-have

#### Screen reader/assistive technology users must be able to navigate through content by headings, block items, lines, words and characters.

Priority: Must-have

Sources: [EPUBTest reading-810 : Move to the next block item](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-810),
[EPUBTest reading-1110 : Navigate by lines](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-1110),
[EPUBTest reading-1010 : Navigate by words](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-1110),
[EPUBTest reading-910 : Navigate by characters](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-910)

#### Screen reader/assistive technology users must be able to read continuously from the current position, and be able to pause, then resume reading from the paused reading location.

Priority: Must-have

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

### Screen Reader Support

Effective screen reader support depends not only on well-structured content but also on the reading app's ability to interact seamlessly with assistive technologies. The application or platform must enable screen readers to accurately interpret and present semantic markup, navigation elements, and interactive features to users. This close collaboration between the reading app and screen reader ensures that users can navigate, access, and understand content efficiently. Addressing these technical requirements is essential to provide a fully accessible and usable experience for screen reader users.

#### The user must be able to use their screen reader in the user interface.

The user must be able to navigate and interact with all elements of the app—including menus, dialogs, buttons, and content—using assistive technologies. All interactive components shall provide appropriate semantic labels and roles to support accessibility standards such as WCAG 2.1 and ARIA guidelines.

Priority: Must-have

#### The user must be able to take advantage of their screen reader's ability to leverage semantic markup in the content.

The application must allow users to read publication content using a screen reader. The rendered content must expose the accessibility semantics to the screen reader. Thus headings, lists, tables, images and other semantic elements must be exposed to the screen reader so that it can be interpreted by the screen reader. Furthermore, semantics of links need to be exposed, such as bibliographic or footnote, should be exposed to the screen reader.

Priority: Must-have

#### The user must be able to use their screen reader in a scrolling mode.

The user must be able to use a scrolling (rather than a paginated mode) to enable the use of screen reader features such as navigating to next/previous heading, landmark, graphic, etc.

Priority: Must-have

#### Screen reader users must be able to navigate confidently between internal hyperlinks.

When navigating to another place in the content (for example when using the table of contents, reading a footnote or following an internal hyperlink) the screen reader user must be able to read from the new navigation position.

Priority: Must-have

#### Screen reader users must be able to activate actionable content.

Screen reader users must be able to activate actionable content (such as links, buttons, expandable elements).

Priority: Must-have

#### Screen reader users must be able to return to their previous reading position.

After navigating to a different part of the content (perhaps by following a footnote, internal hyperlink, referring to a glossary entry or going to a different page) the user must be able to return back to their previous reading position.

Priority: Must-have

Source: [reading-710 : Navigate between internal hyperlinks](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-710)

#### Screen reader users must be able to determine their current location without losing thier place.

Screen user readers must be able to get information about their current position in the content (such as section, page number) without losing their reading position.

Priority: Must-have

#### TODO: Screen reader users must be able to use footnotes

Users must be able to detect the reference to a footnote, reach the content of the footnote, read the content of the footnote and provide a mechanism to move back to the original reading position from the footnote.

Priority: Must-have

Source: [reading-420 : Footnote Reading](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-420)

#### The user could use additional navigation features of the reading app.

In addition to the table of contents and other navigation provided by the content creator, the user could use additional navigation features offered by the reading app that will be especially beneficial to print disabled readers. For example, the app could provide navigation by heading, between landmarks, tables, images and  mathematics expressions, irrespective of whether they are in the same content document.

Priority: Could-have

### Read Aloud

In this requirements document the term "read aloud" refers to the app using Text To Speech (TTS) to provide an audio option for text-based content.

Read aloud functionality plays a crucial role in making digital content accessible to people with print disabilities, such as visual impairments, dyslexia, or other reading challenges. By leveraging Text To Speech (TTS) technology, reading apps provide an alternative way to access text-based information through audio, reducing barriers to reading and comprehension. To offer a smooth and flexible listening experience, the reading app must work seamlessly with the TTS engine to manage how text is processed, queued, and delivered. This includes supporting logical reading order, language changes, and user control over playback and navigation. Such close integration ensures that users can access content audibly in a way that meets their individual needs, enhancing independence, inclusivity, and overall usability.

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

The user must be able to select text (e.g. word, phrase, sentence, paragraph) and have that read aloud.

Priority: Must-have

#### The user must be able to listen to the read aloud without having to manually advance to subsequent pages or chapters.

The read aloud must be able to read continuously until the end of the publication unless interupted by the user.

The read aloud could support a sleep function, pausing the read aloud after a user determined period of time.

Priority: Must-have

#### The user must be able to have the content read aloud in the logical reading order.

Priority: Must-have

Source: [reading-210 : All text should be read in the proper order](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-210), 
[ReadAloud-310 : All text should be read in the proper order](https://www.epubtest.org/test-books/read-aloud/2.0.0/ReadAloud-310)

#### The user of read aloud must hear appropriate pauses after headings, paragraphs, list items, etc.

The read aloud must use appropriate pauses after headings, list items etc., rather than reading as if it is one continuous section of text. The read aloud implementation should pay attention to commonly used text content such as numbered heading and lists.

Priority: Must-have

Source: [EPUBTest reading-510 : TTS allows pause for indicating headings, paragraphs, list items, etc](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-510), 
[ReadAloud-510 : Text to Speech handles punctuation and document structure appropriately](https://www.epubtest.org/test-books/read-aloud/2.0.0/ReadAloud-510)

#### The user must be able to view the text being read aloud.

The user must be able to see the text that is being read aloud, and the display must automatically update to keep the spoken text in view. The techniques for changing the text in display might include scrolling the text to keep the text being read in the centre of the display, or displaying a new screen of text and starting again at the top. Note that users may be reading with large text, so additional care should be taken to consider that the complete text of the first and last sentence may not be in view. The user should be able to see the text being read. If starting from the top of the display then the read aloud should start from the first visble text in view (that is, should not read text that is not visible). The display should promptly update to always show the text being read, even if this is partway through a sentence at the bottom of the display.

The user could have the ability to move to a different part of the text whilst the read aloud continues. If viewing a different part of the text the user should be able to initiate the read aloud from a part of the text they select.

The user could have the option to use read aloud without the text displayed.

Priority: Must-have

#### The user must be able to visually emphasize the text being read aloud and be able to turn this feature off.

The user must be able to visually emphasize the text as it is read aloud using a contrasting highlight, underlining, or other means. Some users will be hindered by this visual cue, e.g. due to health concerns such as epilepsy. Overly granular, like word-by-word highlighting could also be distracting.

The user must be able to to turn off the read aloud visual emphasis.

Priority: Must-have

Source: [ReadAloud-610 : Text is emphasised as it is spoken by read aloud](https://www.epubtest.org/test-books/read-aloud/2.0.0/ReadAloud-610)

#### The user must be able to change the color or style of the visual emphasis.

The user must be able to adjust the visual emphasis.

The user could be able to adjust the number of words that are highlighted at any time.

Priority: Must-have

Source: [ReadAloud-610 : Text is emphasised as it is spoken by read aloud](https://www.epubtest.org/test-books/read-aloud/2.0.0/ReadAloud-610)

#### The user of read aloud must hear content in the correct language.

The user must be able to hear the read aloud using the correct voice when reading content with language tags (if available to the reading app). The user should be able to override language switching and select the language to be used for all content.

The read aloud could switch between dialects of the same language. If this feature is supported the user must be able to disable it.

Priority: Must-have

Source: [reading-1510 : TTS Change Languages Automatically](https://www.epubtest.org/test-books/non-visual-reading/2.0.0/reading-1510)

#### The user must be able to control the rate of the read aloud.

The user must be able to choose the speed of the read aloud voice. The reading app must not distort the pitch when the user has selected higher listening speeds.

The reading app could provide an audio preview to assist the user in selection.

Priority: Must-have

#### The user must be able to control the voice of the read aloud.

The user must be able to select from a range of voices.

Consideration should made of how the voice options are presented (by region or language, online/offline, etc). The reading app could provide an audio preview to assist the user in their selection.

Priority: Must-have

Source: [ReadAloud-400 : Change Read Aloud reading voice](https://www.epubtest.org/test-books/read-aloud/2.0.0/ReadAloud-400)

#### The user must be able to listen to image alt text.

The read aloud feature must be able to announce the alt text of images. 

The user must be able to turn off the read aloud of image alt text. The user should be able to escape from the image alt text once the read aloud has started.

The image alt text could be distinguished from text content with an announcement, use of different voice, or other technique.

Priority: Must-have

#### The user must be able to listen to math content when using read aloud.

The read aloud feature must be able to announce encoded math content (eg MathML).

The user should be able to adjust the announcement of math content according to their preference (eg relative reading speed,  reading style, verbosity).

Priority: Must-have

#### The user must be able to lock their mobile device and use read aloud.

On a mobile device the user must be lock the device without the read aloud stopping. The user must be able to listen and control read aloud (pause, resume, go back and forward) from the lock screen, to the extent this is supported on the platform. The display could show relevant information such as the current position in the title.

Editor's note - this probably also applies to audio playback.

Priority: Must-have

#### The user must be able to control read-aloud playback using the device’s media controls.

If supported on the device and platform the user must be able to control read-aloud playback using the device’s media controls, such including play, pause, skip forward, skip backward, and stop functions on a keyboard or headset.

Priority: Must-have

#### The user must be able to use read aloud with tables.

The read aloud must read the table contents from left to right and top to bottom. The read aloud could indicate the start of the table though an announcement or other notification.

Priority: Must-have.

#### **The user must be able to use read aloud with expandable/collapsable content**

Expanded content must be read aloud. Collapsed content must not be read aloud.

Priority: Must-have.

#### The user must be able escape from certain structures when using read aloud.

The user must be able to control the read aloud so they can escape from reading all the way through escapable items and to continue read aloud from the item following the table.

The escapable items are defined by each format specification.

Priority: Must-have.

Source: https://github.com/readium/guided-navigation/blob/main/roles.md#list-of-escapable-roles

#### The user must be able to decide the read aloud should skip over certain content.

The user must be able to configure their reading app so that it does not announce skipable elements. 

The user preference for skipping non-core content could be set on a per-title basis.

The skippable items are defined by each format specification.

Priority: Must-have

Sources: https://daisy.org/activities/standards/daisy/daisy-2/daisy-2-02-skippable-structures-recommendation/#intro_1, https://github.com/readium/guided-navigation/blob/main/roles.md#list-of-skippable-roles

#### The user could be able to choose from a range of read aloud modes.

The user could be able to set the mode so that read aloud is not continuous. The amount read should be chosen by the user (eg read aloud stop after each word, sentence, paragraph, page or chapter). 

Priority: Could-have

#### The user could be able to adjust read aloud to change the pause length between content blocks.

The user could be able to adjust the pauses between sentences, paragraphs, etc.

Priority: Could-have

#### The user could be able to choose to have semantic expressiveness for read aloud.

The user could be able to adjust the pitch or style for emphasized text (eg bold, italic, underlined). If this feature is supported the user must be able to disable it.

Priority: Could-have

### Visual Adjustments

Flexible display options in a reading app are essential for people with print disabilities, especially those with low vision or dyslexia. Allowing users to customize the visual presentation of text and images — including font type, size, color contrast, spacing, and margins — significantly improves readability and comfort. These adaptations reduce visual stress and cognitive load, making it easier for users to process and understand content. By removing visual barriers, reading apps become more accessible, empowering users to have a more personalized and effective reading experience.

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

#### The user must be able change the line spacing, word spacing and letter spacing.

The amount of line spacing (leading), word spacing (space between words) and letter spacing (space between letters/characters) impacts readability. Some people need more space to read text and will have individual preferences. Line spacing also helps with tracking.

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

Priority: Must-have

Sources: [Accessibility Requirements for People with Low Vision: margins and borders](https://w3c.github.io/low-vision-a11y-tf/requirements.html#margins-and-borders),
[Shorter Lines Facilitate Reading in Those Who Struggle](https://doi.org/10.1371/journal.pone.0071161)

#### The user must be able to view the content in a scrolling view.

For reflowable content, if the reader offers a paginated view, then the user should also be able to vie it in a scrollabe view.

Priority: Must-have

#### The user must be able to enlarge images.

The user should be able to select an image and make it larger. There should be controls to adjust the size and to pan around an image when it no longer fits within the display.

A custom color theme used for viewing the text can sometimes render parts of the image difficult to see. There could be the option in the image viewer to revert to the default color mode, or to choose different color themes.

Priority: Must-have

Source: [visual-710 : Enlarge SVG Images](https://www.epubtest.org/test-books/visual-adjustments/2.0.0/visual-710)

#### The user must be able to adjust the size and color of math expressions by adjusting the text's font size and color.

Math expressions included as MathML (or LaTeX, if supported) should be displayed correctly. As the user adjusts the size and colors of the text content, the math expressions should change accordingly. As the text size is increased, so should the math expressions in proportion. As the user changes the colors for the text content, this should also affect the math expressions.

Priority: Must-have

Source: [visual-550 : Viewing MathML](https://www.epubtest.org/test-books/visual-adjustments/2.0.0/visual-550)

#### The user must be able to personalize the background and foreground colors.

The user should be able to set the background and text color from the full color spectrum.

Some people need high contrast between text and background, including many older people who lose contrast sensitivity from ageing. Some read better with dark text on light background. Others find it easier to read with low contrast and colors that present less glare.

For some people, common color combinations or colors from a limited color palette work fine, for example, black text on white background or the inverse with white text on black background. For instance, black text on a white background is specifically useful for people with dyslexia. Other people need to select more specific background and text colors. For example, people who need low brightness overall, need to select the specific background and text colors that provide sufficient contrast for them yet not too high brightness. Readable and optimal color combinations differs vastly among individuals and can even vary for one individual depending on conditions such as fatigue and lighting.

Priority: [Must-have for a limited color palette; Should-have for more specific background and text colors]

Sources: [visual-110 : Change background and foreground color](https://www.epubtest.org/test-books/visual-adjustments/2.0.0/visual-110), [Accessibility Requirements for People with Low Vision: text contrast](https://w3c.github.io/low-vision-a11y-tf/requirements.html#text-contrast)

#### The user must be able to use the app with the high contrast and magnification features of the operating system platform.

Some people use high contrast modes on their device because it increases readability by maximizing the difference between text and background. Some people use the magnification feature of the operating system, or third party tools, to increase the size of text and images on the display.

Users must be able to use these features with the reading app. The app should respect the high contrast settings chosen by the user.

Priority: Must-have

Source: [visual-310 : Apply high contrast system configuration](https://www.epubtest.org/test-books/visual-adjustments/2.0.0/visual-310)

#### The user must be able to change the display brightness.

Some individuals with low vision or dyslexia may have photophobia or light sensitivity. The ability to dim the screen can make reading more comfortable for these users. For some people with age-related macular degeneration, brighter illumination has been shown to improve reading acuity, critical print size, and maximum reading speed. Adjusting brightness can enhance the contrast between text and background, making it easier for individuals with low vision to distinguish letters and words.

The user must be able to adjust the display brightness when using the reading app. If this is not possible on the device or the operating system, it must be possible in the reading app itself.

If it is possible to adjust the display brightness on the device or in the operating system, it could be possible in the reading app itself.

Priority: Must-have

[visual-210 : Change brightness](https://www.epubtest.org/test-books/visual-adjustments/2.0.0/visual-210),
Legge G. E. (2016). Reading Digital with Low Vision. Visible language, 50(2), 102–125. (https://pmc.ncbi.nlm.nih.gov/articles/PMC5726769/)

#### The user should be able to remove the visual text styling (underline, italic, bold).

For some people, it is difficult to read text that is italicized, underlined or bold. Users should have the option to view the text without these visual formatting styles. However, underlining should be retained for hyperlinks. While removing formatting may result in the loss of some semantic significance, users should be able to toggle back to the visually formatted version as needed.

Priority: Should-have

Sources: [Accessibility Requirements for People with Low Vision: text style](https://w3c.github.io/low-vision-a11y-tf/requirements.html#style)

#### The user should be able to visually emphasize the text being read using a contrasting highlight, ruler lines, deemphasizing the surrounding text, or other means.

There are many ways this can be done. Here are some implementation examples: [...]

Priority: Should-have

Source: [ReadAloud-610 : Text is emphasised as it is spoken by read aloud](https://www.epubtest.org/test-books/read-aloud/2.0.0/ReadAloud-610)

#### The user should be able to enlarge math expressions for closer inspection.

Math expressions often contain small symbols such as exponents, indices, dot notations and derivatives. It should be possible for the user to view a math expression as a separate item and enlarge it.

Priority: Should-have

#### The user could be able change the capitalization of text to sentence style.

Text written in all capital letters or all small capital letters is more difficult to read for most people, with and without disabilities. Users should have the option to choose a sentence-style version. Acronyms that are correctly marked as abbreviations will remain in uppercase; otherwise, they will be converted to sentence style. Users should also be able to toggle between the different styles as needed.

Priority: Could-have

Sources: [Accessibility Requirements for People with Low Vision: capitalization](https://w3c.github.io/low-vision-a11y-tf/requirements.html#capitalization)

#### The user could be able to view the content in a paginated view.

For many users a scrolling view is preferable, some may prefer a paginated view.

Priority: Could-have

#### The user could be able [to flatten the colors of math expressions].

Certain parts of math expressions are sometimes presented in special colors, e.g. superscript in red. For some people this can present problems. The user could be able to remove the color formatting used in math expressions so the chosen text color is always used.

Priority: Could-have

### Making Notes

The ability to add, review, and edit notes within a reading app is an important feature for many users, especially those with print disabilities or learning challenges. Notes provide a flexible way to capture thoughts, highlight important information, or add personal annotations, which can aid comprehension and retention. For users who rely on assistive technologies, well-integrated note functionality (such as audio notes, easy navigation, and synchronization) ensures that these annotations are accessible and usable across different contexts and devices. Supporting notes alongside the text also enhances interactivity and engagement with the content, making the reading experience more personalized and effective.

This section had a good discussion in the working group and will now be written up by the editors.

#### TODO: The user should be able to add, review and edit notes.

Sources: [EPUBTest anno-210 : Add a note](https://www.epubtest.org/test-books/basic-functionality/2.0.0/anno-210),
[EPUBTest anno-310 : Review and navigate Notes](https://www.epubtest.org/test-books/basic-functionality/2.0.0/anno-310)

#### The user must be able to add notes.

Notes may contain either plain text or audio. It must be possible to insert notes at any position within the running text. Notes must be anchored to at least a text range within a paragraph. The element to which the note is attached must be visually indicated and must be identifiable with any screen reader. 

Priority: Must-have

Sources: [EPUBTest anno-210 : Add a note](https://www.epubtest.org/test-books/basic-functionality/2.0.0/anno-210),
[EPUBTest anno-310 : Review and navigate Notes](https://www.epubtest.org/test-books/basic-functionality/2.0.0/anno-310)

#### The user must be able to view notes alongside the text, for example in the margin.

Priority: Must-have

#### The user must be able to review and edit notes.

Priority: Must-have

#### Screen reader users must be able to navigate from one note to another.

Priority: Must-have

#### The user must be able to save notes automatically, including during offline use.

Notes must be synchronized once the device is online.

Priority: Must-have

#### The user must be able to view previously saved notes when reopening the book.

Priority: Must-have

#### The user should be able to format the content of a note using basic rich text formatting.

Supported formatting includes bold, italic, and underline.

Priority: Should-have

#### The user should be able to hide or show individual notes.

Priority: Should-have

#### The user should be able to hide all notes.

For a more focused experience

Priority: Should-have

#### The user should be able to have a single note read aloud.

Priority: Should-have

#### The user should be able to have all notes read aloud in sequence.

Priority: Should-have

#### The user should be able to synchronize notes across multiple devices.

Priority: Should-have

#### The user should be able to export notes.

Priority: Should-have

#### The user could be able to share notes with others.

#### TODO: The user should be able to add, review and edit highlights.

Priority: Could-have

### TODO: Entering Answers

Entering answers directly within digital publications is a feature that enables active engagement and participation, especially for learners with print disabilities. These users often face significant challenges because if they cannot read or write directly in physical books, and working with separate files for answers can be time-consuming and mentally exhausting. They benefit greatly from being able to enter their responses exactly where the question or prompt appears in the digital content, making the process more intuitive and less fragmented. Supporting a variety of input types—from simple text fields to selection controls—ensures that all users can provide responses effectively and independently. Accessibility considerations, such as screen reader compatibility and the ability to save and edit answers, are essential to create an inclusive and seamless user experience. Moreover, synchronization and export capabilities enhance flexibility, allowing users to access and manage their answers across devices and contexts.

Digital book reading apps have not typically included this functionality. This section is at an early stage of discussion. Input from educators and app developers will be important to craft the requirements in a way that seek to address the opportunity for new learning experiences whilst describing requirements that are achievable.

#### The user must be able to enter answers into input fields provided in a publication.

Text, possibly audio, no MathML in text fields

Priority: Must-have

#### The user must be able to enter different types of answers.

Supported field types:
Single-line text field, Multi-line text field, Radio buttons, Checkboxes, Dropdown menus

Priority: Must-have

#### The user must be able to review and edit answers in the input fields.

Priority: Must-have

#### The user must be able to save answers.

Preferably: automatically. Ambitious aim: save online, so answers can be synchronized across multiple devices. In that case, saving should happen including during offline use. Answers must sync once the device is online.
More modest aim: save locally.

Priority: Must-have

#### Screen reader users must be able to navigate between input fields.

Priority: Must-have

#### The user should be able to format answers in text fields using a basic rich text editor.

Formatting options: bold, italic, underline

Priority: Should-have

#### The user should be able to add custom input fields where none exist.

These must support the same input types, be accessible via screen reader navigation, and be included in exports.

Priority: Should-have

#### The user should be able to see previously saved answers when reopening a book.

Priority: Should-have

#### The user should be able to export answers.

Priority: Should-have

#### The user could be able to synchronize answers across multiple devices.

Priority: Could-have

#### The user could be able to share answers with others (e.g. teachers, students).

Priority: Could-have

#### The user could be able to have their answers automatically checked.

Priority: Could-have

Sources: [EPUBTest anno-010 : Add a Bookmark or Highlight](https://www.epubtest.org/test-books/basic-functionality/2.0.0/anno-010), 
[EPUBTest anno-110 : Review and navigate Bookmarks or Highlights](https://www.epubtest.org/test-books/basic-functionality/2.0.0/anno-110)

### TODO: Switching Modalities

To include switching between embedded audio and read aloud.

### TODO: Library and Bookshelf

To include:

- library- logging in, discovery, download, return
- bookshelf- sorting, adding and removing books
- titles - book information (metadata), book rating/reviewing/recommending

:::
::: {#userstories .section}

## User Stories

The [user stories](https://daisy.github.io/reading-apps-ux-reqs/use-cases/) referenced in this document were developed by the working group.
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
