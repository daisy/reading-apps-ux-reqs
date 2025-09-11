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
[Editors' Working Draft]{.subtitle}

</hgroup>

[11 September 2025]{.pubdate}

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
  - [Embedded Audio](#embedded-audio)
  - [Visual Adjustments](#visual-adjustments)
  - [Clarifying Note on Bookmarks, Notes and Highlights](#clarifying-note-on-bookmarks-notes-and-highlights)
  - [Bookmarking](#bookmarking)
  - [Making Notes](#making-notes)
  - [Highlighting](#highlighting)
  - [Entering Answers](#entering-answers)
  - [Library and Bookshelf](#library-and-bookshelf)
- [Miscellaneous](#miscellaneous)
- [Additional User Requirements for Future Consideration](#additional-user-requirements-for-future-consideration)
- [User Stories](#user-stories)
- [Acknowledgements](#acknowledgements)
- [References](#references)
  

</nav>

::: {#introduction .section}

## Introduction

This document presents a detailed set of user requirements to help
developers, designers, and decision-makers understand what individuals
with diverse print disabilities need and expect from digital reading
solutions- especially when it comes to accessibility, usability, and
inclusive design.

Created through close collaboration between DAISY Consortium members,
people with print disabilities, accessibility experts, and developers of
specialized reading apps, this resource captures a wide range of expert
knowledge and practical insights. The document draws on the lived
experiences of people with print disabilities, and the requirements have
been shaped and articulated by professionals with deep expertise in
accessible reading technology.

This **Editors' Working Draft** represents the results of six
months of working group meetings, workshops, and discussions with
developers. Feedback and collaboration are welcomed as the document
evolves toward the publication, likely in Q4 of 2025.

While the document is particularly relevant for those developing or
procuring specialized reading apps, it also offers valuable guidance for
those working on mainstream reading platforms who wish to make their
products outstandingly accessible and user-friendly for everyone.
Whether you are building a new reading application from the ground up or
enhancing an existing one, we invite you to explore these requirements
not just as a treasure trove of insights into the needs of people with
print disabilities, but as a roadmap toward more inclusive digital
reading experiences.

:::
::: {#userrequirements .section}

## User Requirements

### Navigation

Effective navigation is a critical aspect of digital accessibility.
Users often face challenges in understanding where they are within a
digital publication or application and how to move seamlessly between
sections. For example, screen reader users, who access content
sequentially through synthetic speech or braille displays, rely on
navigation features to rapidly and efficiently orient themselves and
access content efficiently. Readers with learning differences benefit
from clear navigation structures, well-defined headings, and consistent
cues. Understanding and addressing these user requirements is key to
creating inclusive digital experiences that empower all users to
navigate content independently and with ease.

#### The user must have a straightforward way to navigate forward and backward through the content

For content with text it must be possible to move forward and backward
from the currently displayed screen. For content with audio it must be
possible to move forward and backward using time-based navigation.

Priority: Must-have

#### The user must be able to navigate the publication using the Table of Contents

When displaying the table of contents, the focus must be on the entry
that matches the user\'s current reading position. If the publication's
table of content comprises a hierarchy of entries (e.g. volumes,
chapters, subsections) then it must be presented as a tree view, nested
list view or any other view that conveys the structure to the user. The
user must have a mechanism to move between items in the table of
contents of the same level (e.g. between the chapters without having to
go via the subsections).

Page numbers or percentage information could be provided in the table of
contents.

The user could be able to search within the table of contents.

Priority: Must-have

#### The user must have a way to navigate the content by pages

When the publication includes page markup, then it must be possible to
navigate by page numbers. If the publication does not include page
markup it could be possible to navigate by 'pseudo pages' (where the app
uses an algorithm to approximate navigation points equivalent to typical
page lengths).

Priority: Must-have

#### The user must have a way to go to a specific location in audio-based content

When reading audio-based content it must be possible to go to a specific
location. This could be based on time, percentage, or another approach.

Priority: Must-have

#### Screen reader/assistive technology users must be able to navigate through content by headings, block items, lines, words and characters

This functionality is provided by the screen reader or assistive 
technology, but it relies on how the audio and text content is exposed 
within the app. To support navigation by headings, blocks, lines, words, 
and characters, the content must be properly structured and tagged so 
that the screen reader can interpret and present it accurately to the 
user.

Priority: Must-have

#### Screen reader users must be able to read continuously from the current position, and be able to pause, then resume reading from the paused reading location

For content with text it must be possible to use the continuous reading
feature of a screen reader to start, pause and resume continuous
reading. The reading should not stop at the end of the display but
continue until the end is reached or stopped by the user.

Priority: Must-have

#### The user must be able to return to the last location the next time they open the publication

The saving of the user\'s location must happen automatically, for
example when closing the app. When reading text-based content it must be
possible to return to the approximate location (such as the same page or
screen of text). It could be possible to return to the exact last
location.

When reading audio-based content it must be possible to return to the
exact last location.

Priority: Must-have

#### The user must be able to determine their location in the content

The user must be able to get information about their current position in
the publication without losing their reading position. The minimum
information expected is the percentage progress.

The user should be able to determine the current chapter, section, and
current page number where this information is provided in the
publication.

Screen reader users must be able to get information about their current
position in the content without losing their reading position.

Priority: Must-have

#### The user could be able to go back to a previous location in the content

A "go back" feature within the reading application allows users to 
explicitly return to a previous location after navigating through a 
digital publication, for example, after following an internal link, 
jumping to a search result, or accessing a glossary entry. While some 
screen readers offer limited navigation history, an in-app "go back" 
function provides a more predictable and user-controlled experience, and 
it benefits users who do not use screen readers as well. This is 
particularly beneficial for users with print disabilities, as it 
supports orientation and reduces cognitive load. The application could 
optionally support multiple location histories to enhance usability 
across complex publications.

Priority: Could-have

### Screen Reader Support

Effective screen reader support depends not only on well-structured
content but also on the reading app's ability to interact seamlessly
with assistive technologies. The application or platform must enable
screen readers to accurately interpret and present semantic markup,
navigation elements, and interactive features to users. This close
collaboration between the reading app and screen reader ensures that
users can navigate, access, and understand content efficiently.
Addressing these technical requirements is essential to provide a fully
accessible and usable experience for screen reader users.

#### The user must be able to use their screen reader in the user interface

The user must be able to navigate and interact with all elements of the
app---including menus, dialogs, buttons, and content---using their
assistive technology. All interactive components shall provide
appropriate semantic labels and roles to support accessibility standards
such as WCAG 2.1 and ARIA guidelines.

Priority: Must-have

#### The user must be able to take advantage of their screen reader's ability to leverage semantic markup in the content

The application must allow users to read publication content using a
screen reader. The rendered content must expose the accessibility
semantics to the screen reader. Thus headings, lists, tables, images,
and other semantic elements must be exposed to the screen reader so that
it can be interpreted by the screen reader. Where present, the semantics
of links---such as whether they are bibliographic references or
footnotes---should be made available to screen readers.

Priority: Must-have

#### The user must be able to use their screen reader in a scrolling mode

The user must be able to use a scrolling (rather than a paginated mode)
to enable the use of screen reader features (such as navigating to
next/previous heading, landmark, graphic, etc.).

Priority: Must-have

#### Screen reader users must be able to navigate confidently between internal hyperlinks

When navigating to another place in the content (for example when using
the table of contents, reading a footnote or following an internal
hyperlink) the screen reader user must be able to read from the new
navigation position.

Priority: Must-have

#### Screen reader users must be able to activate actionable content

Screen reader users must be able to activate actionable content (such as
links, buttons, expandable elements).

Priority: Must-have

#### Screen reader users must be able to return to their previous reading position

After navigating to a different part of the content, such as following a 
footnote, internal hyperlink, glossary entry, or switching to another 
page, the user must be able to return to their previous reading 
position. Most modern screen readers support navigation history or 
reading position memory, allowing users to jump back to where they left 
off. To enable this functionality effectively, the application must 
maintain focus and structural consistency, ensuring that the screen 
reader can track and restore the user's position within the content.

Priority: Must-have

#### Screen reader users must be able to use footnotes and endnotes

Users must be able to detect the reference to a footnote (or endnote),
reach the content of the footnote, read the content of the footnote, and
provide a mechanism to move back to the original reading position from
the footnote.

Priority: Must-have

#### The user could use additional navigation features of the reading app

In addition to the table of contents and other navigation provided by
the content creator, the user could use additional navigation features
offered by the reading app. Such navigation affordances are especially
beneficial to print disabled readers. For example, the app could provide
navigation by heading, between landmarks, tables, figures, and
mathematics expressions, irrespective of whether they are in the same
content document.

Priority: Could-have

### Read Aloud

Note: In this document the term "read aloud" refers to the app
leveraging Text to Speech (TTS) to provide an audio option for
text-based content. This is distinct from embedded audio.

Read aloud functionality plays a crucial role in making digital content
accessible to people with visual impairments, dyslexia, or other reading
challenges. By leveraging Text to Speech (TTS) technology, reading apps
provide a complementary or alternative way to access text-based
information through audio, reducing barriers to reading and
comprehension. To offer a smooth and flexible listening experience, the
reading app must work seamlessly with the TTS engine to support logical
reading order, language changes, and provide the user control over
playback and navigation.

#### The user must be able to listen to text-based content using synthetic speech (Text To Speech)

The user must be able to use a TTS read aloud feature for text-based
content. If the publication also has text synchronized with embedded
audio, then the user must be able to choose the alternative of listening
to the TTS read aloud.

Priority: Must-have

#### The user must be able to control the starting position of the read aloud

The user must be able to choose the position from where the read aloud
begins.

If a screen reader is being used, then the read aloud should start from
the screen reader position.

If a screen reader is not being used, then:

- if the user has indicated a start position, then read aloud should
  start from there.
- if the user has made no selection, then read aloud should start from
  an approximate reading position (e.g., the first visible text on the
  display).

Priority: Must-have

#### The user must be able to read aloud selected parts of the content

The user must be able to select text (e.g., word, phrase, sentence,
paragraph) and have that read aloud.

Priority: Must-have

#### The user must be able to listen to the read aloud without having to manually advance to subsequent pages or chapters

The app must be able to continuously read aloud until the end of the
publication, unless interrupted by the user.

The read aloud could support a sleep function, pausing the read aloud
after a user determined period of time.

Priority: Must-have

#### The user must be able to have the content read aloud in the logical reading order

Priority: Must-have

#### The user of read aloud must hear appropriate pauses after headings, paragraphs, list items, etc.

The read aloud must use appropriate pauses after headings, list items
etc., rather than reading as if it is one continuous section of text.
The read aloud implementation should pay attention to commonly used text
content such as numbered headings and lists.

Priority: Must-have

#### The user must be able to view the text being read aloud

The user must be able to see the text that is being read aloud, and the
display must automatically update to keep the spoken text in view. The
techniques for changing the text in display might include scrolling the
text to keep the text being read in the center of the display, or
displaying a new screen of text and starting again at the top. Note that
users may be reading with large text, so additional care should be taken
to consider that the complete text of the first and last sentence may
not be in view.

The user should be able to see the text being read. If starting from the
top of the display then the read aloud should start from the first
visible text in view (that is, the app should not read text that is not
visible). The display should promptly update to always show the text
being read, even if this is partway through a sentence at the bottom of
the display.

The user could have the ability to move to a different part of the text
whilst the read aloud continues. If viewing a different part of the
text, the user should be able to initiate the read aloud from a part of
the text they select.

The user could have the option to use read aloud without the text
displayed.

Priority: Must-have

#### The user must be able to visually emphasize the text being read aloud and be able to turn this feature off

The user must be able to visually emphasize the text as it is read aloud
using a contrasting highlight, underlining, or other means. Some users
will be hindered by this visual cue, so the user must be able to turn
off the read aloud visual emphasis.

Priority: Must-have

#### The user must be able to change the color or style of the visual emphasis

The user must be able to adjust the visual emphasis. The user could be
able to adjust the number of words that are highlighted at any time.

Priority: Must-have

#### The user of read aloud must hear content in the correct language

The user must be able to hear the read aloud using the correct voice
when reading content with language tags (if available to the reading
app). The user should be able to override language switching and select
the language to be used for all content.

The read aloud could switch between dialects of the same language. If
this feature is supported the user must be able to disable it.

Priority: Must-have

#### The user must be able to control the rate of the read aloud

The user must be able to choose the speed of the read aloud voice. The
reading app must not distort the pitch when the user has selected higher
listening speeds.

The reading app could provide an audio preview of the adjusted rate to
assist the user in selection.

Priority: Must-have

#### The user must be able to control the voice of the read aloud

The user must be able to select from a range of voices.

Consideration should made of how the voice options are presented (by
region or language, online/offline, etc). The reading app could provide
an audio preview to assist the user in their selection of voices.

Priority: Must-have

#### The user must be able to listen to image alt text

The read aloud feature must be able to announce the alt text of images.

The user must be able to turn off the read aloud of image alt text. The
user should be able to escape from the image alt text once the read
aloud has started.

The image alt text could be distinguished from text content with an
announcement, use of different voice, or other technique.

Priority: Must-have

#### The user must be able to listen to math content when using read aloud

The read aloud feature must be able to announce encoded math content
(e.g. MathML).

The user should be able to adjust the announcement of math content
according to their preference (e.g. relative reading speed, reading
style, verbosity).

Priority: Must-have

#### The user must be able to lock their mobile device and use read aloud

On a mobile device the user must be able to lock the device without the
read aloud stopping. The user must be able to listen and control read
aloud from the lock screen, to the extent this is supported on the
platform (e.g., pause, resume, go back and forward). The display could
show relevant information such as the current position in the title.

Editor's note - this probably also applies to audio playback.

Priority: Must-have

#### The user must be able to control read-aloud playback using the device's media controls

If supported on the device and platform the user must be able to control
read-aloud playback using the device's media controls, such including
play, pause, skip forward, skip backward, and stop functions on a
keyboard or headset.

Priority: Must-have

#### The user must be able to use read aloud with tables

The read aloud must read the table contents from left to right and top
to bottom. The read aloud could indicate the start of the table though
an announcement or other notification.

Priority: Must-have.

#### The user must be able to use read aloud with expandable/collapsable content

Expanded content must be read aloud. Collapsed content must not be read
aloud.

Priority: Must-have.

#### The user must be able to escape from certain structures when using read aloud

The user must be able to control the read aloud so they can avoid
reading all the way through escapable items and to continue read aloud
from the following item (e.g. a table).

Each format specification defines which items can be escaped.

Priority: Must-have.

#### The user must be able to decide that the read aloud should skip over certain content

The user must be able to configure their reading app so that it does not
announce skippable elements.

The user preference for skipping non-core content could be set on a
per-title basis.

Each format\'s specification determines which items can be skipped.

Priority: Must-have

#### The user could be able to choose from a range of read aloud modes

The user could be able to set the mode so that reading aloud is not
continuous. Users should decide how much they want to read (e.g. read
aloud then stop after each word, sentence, paragraph, page, or chapter).

Priority: Could-have

#### The user could be able to adjust read aloud to change the pause length between content blocks

The user could be able to adjust the pauses between sentences,
paragraphs, etc.

Priority: Could-have

#### The user could be able to choose to have semantic expressiveness for read aloud

The user could be able to adjust the pitch or style for emphasized text
(eg bold, italic, underlined). If this feature is available, users
should have the option to turn it off.

Priority: Could-have

### Embedded Audio

Note: In this document the term "embedded audio" refers to the audio
content (could be human narrated audio or generated Text to Speech) that
is provided as part of the publication. This is distinct from read
aloud, where the app dynamically uses on device or cloud TTS to create
an audio rendition whilst reading the publication.

Embedded audio includes both audio-only publications and synchronized
audio-text formats, where the audio is aligned with the visual text.
Audio-only formats are a long-standing favorite among people with print
disabilities, offering a streamlined, immersive listening experience.
They are also increasingly popular in mainstream contexts, such as for
multitasking or screen-free reading.

Synchronized audio-text formats offer additional benefits by enabling
users to follow the structure of the text while listening. This supports
a wide range of reading strategies---for example, allowing users to
navigate the text with assistive technologies, adjust playback speed or
verbosity, or combine listening with reading for improved comprehension
and control. Although this functionality is not yet widely supported in
reading systems, it holds great potential for inclusive and flexible
reading experiences.

This section outlines the core user requirements for interacting with
embedded audio, including playback control, synchronization with text,
visual emphasis, and customization. These features ensure that users can
access high-quality narration in a way that aligns with the structure
and intent of the publication.

While synchronized playback is well covered here, the ability to switch
flexibly between listening and reading modes---such as pausing narration
to read with a screen reader and resuming from the same point---is not
yet addressed and remains an area for future development.

#### The user must be able to access and play pre-recorded audio (human-narrated or pre-recorded TTS)

The reading system must support pre-recorded audio playback
(human-narrated or pre-recorded TTS), whether synchronized with the text
or provided as audio-only. Where synchronized audio is available,
users must have the option to switch to TTS read aloud.

Priority: Must-have

#### The user must be able to control the starting position of the embedded audio

The user must have a way to start reading from a specific location in
embedded audio content.

When reading publications with embedded audio it must be possible to go
to a specific location. This could be based on time, percentage, or
another approach.

Priority: Must-have

#### The user must be able to listen to the embedded audio without having to manually advance to subsequent pages or chapters

The reading system must support uninterrupted playback of embedded audio
across sections or chapters, allowing users to listen continuously
without needing to manually advance. Playback should only stop if the
user chooses to pause or exit, or at the end of the publication.

To support flexible listening, the system must also offer a sleep timer
that pauses playback after a user-defined duration.

Priority: Must-have

#### The user must be able to listen to embedded audio content in the correct logical reading order, matching the intended structure of the publication

To ensure a coherent listening experience, the reading system must play
embedded audio in the correct reading order. For audio-only
publications, this typically follows the sequence of audio files as
defined by the publication. In synchronized text and audio formats, the
playback order must be determined by the markup that links text and
audio, ensuring that the spoken content aligns with the visual
structure.

Priority: Must-have

#### The user must be able to view the corresponding text while listening to embedded audio, if synchronized text is available

When embedded audio is synchronized with text, the user must be able to
see the relevant text, and the display must automatically update to keep
the spoken text in view. The techniques for changing the text in display
might include scrolling the text to keep the text being read in the
center of the display or displaying a new screen of text and starting
again at the top. Keep in mind that some users may use large text
settings, so it\'s important to consider that they might not see the
entire first or last sentence.

The user should be able to see the text being read. If starting from the
top of the display then the audio playback should start from the first
visible text in view (that is, should not read text that is not
visible). The display should promptly update to always show the text
being read, even if this is partway through a sentence at the bottom of
the display.

The user could have the ability to move to a different part of the text
whilst the playback continues. If viewing a different part of the text,
the user should be able to initiate the playback from a part of the text
they select.

The user could have the option to listen to the audio without displaying
the text.

For audio-only publications without synchronization, this requirement
does not apply.

Priority: Must-have

#### The user must be able to enable or disable visual emphasis of synchronized text during embedded audio playback, if synchronized text is available

When synchronized text is available, the user must be able to visually
emphasize the text currently being played in the embedded audio. This
may include highlighting, underlining, or other visual cues. Some users
benefit from fine-grained emphasis, such as word-by-word highlighting,
which can support focus and comprehension. However, others may find this
distracting or experience negative effects due to visual sensitivity. To
accommodate diverse needs, users must be able to turn visual emphasis on
or off, and systems should consider offering options to adjust the
granularity of the emphasis.

Priority: Must-have

#### The user must be able to customize the color and style of the visual emphasis applied to synchronized text during embedded audio playback, if synchronized text is available

The user must be able to adjust the visual emphasis of the synchronized
text and audio.

The user could be able to adjust the number of words that are
highlighted at any time.

Priority: Must-have

#### The user must be able to adjust the playback speed of embedded audio without distortion of pitch

The user must be able to control the playback rate of embedded audio,
enabling faster or slower listening according to their preference.
Playback speed adjustments must preserve the natural pitch of the audio
to maintain clarity and intelligibility. To support user
decision-making, the system could offer a preview of the audio at the
selected speed before applying the change.

Priority: Must-have

#### The user must be able to listen to alt texts included in embedded audio, and must be able to disable or skip them if supported by the publication

If image descriptions are included in the embedded audio as alt texts,
the reading system must allow users to hear them as part of the
playback. To support user preferences and accessibility needs, users
must be able to disable or skip these descriptions, provided the
publication includes the necessary markup or audio segmentation. Where
possible, image descriptions should be distinguishable from surrounding
content---such as through a brief introductory phrase, or audio cue.

Priority: Must-have

#### The user must be able to listen to math content included in embedded audio, if present in the publication

If math content is included in the embedded audio (e.g., MathML), the
reading system must ensure it is presented clearly and accessibly as
part of the narration. The playback feature must be able to announce
encoded math content.

The user should be able to adjust the announcement of math content
according to their preference (e.g. relative reading speed, reading
style, verbosity).

Priority: Must-have

#### The user must be able to lock their mobile device and continue listening to embedded audio

When the user locks their mobile device, the embedded audio playback
must continue uninterrupted. The user must be able to listen and control
playback (pause, resume, skip backward, and skip forward) using lock
screen media controls, to the extent that the operating system supports
this functionality. The display could show relevant playback
information, such as the current chapter or time position in the title.

Priority: Must-have

#### The user must be able to control embedded audio playback using device-level media controls

The user must be able to control embedded audio playback using the
device's media controls, such as keyboard shortcuts, headset buttons, or
other hardware interfaces. The user must be able to perform actions like
play, pause, skip forward, skip backward, and stop, if supported by the
platform.

Priority: Must-have

#### The user must be able to listen to embedded audio that accurately conveys the structure and content of tables

When tables are included in the publication, the embedded audio must
present the content in a clear and logical order, typically left to
right, top to bottom, to reflect the table's structure. The user must be
able to understand the relationships between rows and columns through
the narration. If supported by the publication, the audio could include
cues to indicate the start of a table or transitions between cells, such
as spoken labels or brief announcements.

Priority: Must-have.

#### The user must be able to listen to embedded audio that reflects the current state of expandable or collapsible content, playing only content that is expanded

When embedded audio is synchronized with structured content that
includes expandable or collapsible sections, the user must be able to
hear only the content that is currently expanded. Collapsed sections
must be excluded from playback unless the user expands them. This
ensures that the audio experience matches the user's navigation and
content visibility preferences. The reading system must respect the
current document state when determining which audio segments to play.

Priority: Must-have.

#### The user must be able to escape from defined structures during embedded audio playback and resume listening from the item that follows

The user must be able to interrupt playback of certain structures---such
as tables or footnotes---and continue listening from the next item in
the reading order. These escapable structures must be defined by the
publication format and appropriately marked to support this behavior.

Priority: Must-have.

#### The user must be able to configure embedded audio playback to skip content marked as skippable

The user must be able to set preferences that cause embedded audio
playback to skip over content defined as skippable, such as footnotes or
page numbers. These preferences could be set on a per-title basis.
Skippable structures are defined by each format specification.

The user must be able to configure their reading app so that it does not
announce skippable elements.

Priority: Must-have

#### The user could be able to play embedded audio for a selected portion of the text, if the content is synchronized

If the embedded audio is synchronized with the text, the user could
select specific portions such as a word, sentence, or paragraph, and
play the corresponding audio. This feature supports focused listening
and improved navigation but depends on the availability of fine-grained
synchronization in the publication.

Priority: Could-have

#### The user could be able to choose from different playback modes for embedded audio, including non-continuous playback based on content units, if supported by the publication

The user could configure embedded audio playback to stop after specific
units such as a word, sentence, paragraph, page, or chapter. This allows
for more controlled listening and supports focused reading strategies.
Availability of these modes depends on the level of synchronization
provided in the publication.

Priority: Could-have

#### The user could be able to adjust the pause length between content blocks during embedded audio playback, if supported by the publication

The user could configure the length of pauses between sentences,
paragraphs, or other content blocks during embedded audio playback. This
feature may support improved comprehension and comfort, particularly for
neurodivergent users who benefit from controlled pacing. Availability
depends on how the audio is authored and segmented.

Priority: Could-have

### Visual Adjustments

Flexible display options in a reading app are essential for people with
print disabilities, especially those with low vision or dyslexia.
Allowing users to customize the visual presentation of text and images
--- including font type, size, color contrast, spacing, and margins ---
significantly improves readability and comfort. These adaptations reduce
visual stress and cognitive load, making it easier for users to process
and understand content. By removing visual barriers, reading apps become
more accessible, empowering users to have a more personalized and
effective reading experience.

#### The user must be able to change the typeface

The user must be able to change the typeface of all text, choosing
from a range including sans serif and serif fonts. Individuals with low
vision or dyslexia often have specific preferences for font styles that
optimize their reading experience. Typefaces with preferred letter
shapes can aid in visual processing, improve comprehension, and reduce
cognitive load.

Priority: Must-have

#### The user must be able to change the font weight

For some people, bold text is easier to read. Many typefaces have a bold
font and some offer variable weight. The user must be able to select a
typeface with a bold weight. The user could be able to adjust the weight
of selected typefaces.

Visual readability of text requires good visual contrast. Visual
contrast is a product of the text characteristics, such as font weight
(thickness, font stroke width) and font size, the lightness/darkness
difference of the colors used for the text and the background, and other
factors.

Priority: Must-have

#### The user must be able to change the text size

Some people need to increase the size of text in order to read it.
Although increasing size is most common, some people with tunnel vision
and good visual acuity may prefer to decrease the size so they can see
more text at a time.

Priority: Must-have

#### The user must be able to change the line spacing, word spacing and letter spacing

The amount of line spacing (leading), word spacing (space between words)
and letter spacing (space between letters/characters) impacts
readability. People have different space requirements for reading text.
Some people increase line spacing to help with tracking.

Priority: Must-have

#### The user must be able to turn off justification and center-alignment of blocks of text

Justification impacts readability and tracking. Fully justified text
creates uneven spaces between words and letters, leading to "rivers of
white space" that disrupt reading flow and visual tracking, particularly
for people with dyslexia. Users with low vision who rely on screen
magnifiers may encounter exaggerated gaps or overlapping characters in
justified text, making it harder to read. Center-aligned text is also
problematic for multi-line blocks, as it disrupts smooth reading flow
and makes it harder to find the beginning of lines. Depending on the
reading order of the language concerned (left to right, or right to
left) turning the justification or center-alignment off results in a
left-aligned or right-aligned text.

Priority: Must-have

#### The user must be able to change the margins and adjust the line length for blocks of text

Having wide margins results in shorter line lengths. This may be useful
for individuals with certain learning disabilities. Wide margins around
paragraphs can make it easier for some individuals to concentrate on the
main text and avoid distractions from surrounding content.

Conversely, wide margins can make line length too short for people who
use large text.

Priority: Must-have

#### The user must be able to view the content in a scrolling view

For reflowable content, if the reader offers a paginated view, then the
user should also be able to view it in a scrollable view.

Priority: Must-have

#### The user must be able to enlarge images

The user should be able to select an image and make it larger. There
should be controls to adjust the size and to pan around an image when it
no longer fits within the display.

A custom color theme used for viewing the text can sometimes render
parts of the image difficult to see. There could be the option in the
image viewer to revert to the default color mode, or to choose different
color themes.

Priority: Must-have

#### The user must be able to adjust the size and color of math expressions by adjusting the text's font size and color

Math expressions written in MathML or LaTeX (when that format is
supported) need to be shown properly. As the user adjusts the size and
colors of the text content, the math expressions should change
accordingly. When the text is enlarged, the math expressions should also
grow accordingly. As the user changes the colors for the text content,
this should also affect the math expressions.

Priority: Must-have

#### The user must be able to personalize the background and foreground colors

The user should be able to set the background and text color from the
full color spectrum.

Some people need high contrast between text and background, including
many older people who lose contrast sensitivity from ageing. Some
individuals prefer reading dark text on a light background. Others find
it easier to read with low contrast and colors that present less glare.

For some people, common color combinations or colors from a limited
color palette work fine, for example, black text on white background or
the inverse with white text on black background. For instance, black
text on a white background is specifically useful for people with
dyslexia. Other people need to select more specific background and text
colors. For example, people who need low brightness overall, need to
select the specific background and text colors that provide sufficient
contrast for them yet not too high brightness. Readable and optimal
color combinations differs vastly among individuals and can even vary
for one individual depending on conditions such as fatigue and lighting.

Priority: \[Must-have for a limited color palette; Should-have for more
specific background and text colors\]

#### The user must be able to use the app with the high contrast and magnification features of the operating system platform

Some people use high contrast modes on their device because it increases
readability by maximizing the difference between text and background.
Some users enlarge text and images on their screens using built-in
magnifiers or third-party tools.

Users must be able to use these features with the reading app. The app
should respect the high contrast settings chosen by the user.

Priority: Must-have

#### The user must be able to change the display brightness

Some individuals with low vision or dyslexia may have photophobia or
light sensitivity. The ability to dim the screen can make reading more
comfortable for these users. For some people with age-related macular
degeneration, brighter illumination has been shown to improve reading
acuity, critical print size, and maximum reading speed. Adjusting
brightness can enhance the contrast between text and background, making
it easier for individuals with low vision to distinguish letters and
words.

The user must be able to adjust the display brightness when using the
reading app. If this is not possible on the device or the operating
system, it must be possible in the reading app itself.

If it is possible to adjust the display brightness on the device or in
the operating system, it could be possible in the reading app itself.

Priority: Must-have

[visual-210 : Change
brightness](https://www.epubtest.org/test-books/visual-adjustments/2.0.0/visual-210),
Legge G. E. (2016). Reading Digital with Low Vision. Visible language,
50(2), 102--125. (https://pmc.ncbi.nlm.nih.gov/articles/PMC5726769/)

#### The user should be able to remove the visual text styling (underline, italic, bold)

Some people find italicized, underlined, or bold text hard to read.
Users should have the option to view the text without these visual
formatting styles. Nonetheless, hyperlinks should continue to have
underlining. While removing formatting may result in the loss of some
semantic significance, users should be able to toggle back to the
visually formatted version as needed.

Priority: Should-have

#### The user should be able to visually emphasize the text being read using a contrasting highlight, ruler lines, deemphasizing the surrounding text, or other means

The application should provide visual focus indicators to aid reading.
This might include text highlighting, a horizontal bar or translucent
strip that follows the line of text being read, dimming, blurring or
masking the text not currently being read.

Priority: Should-have

#### The user should be able to enlarge math expressions for closer inspection

Math expressions often contain small symbols such as exponents, indices,
dot notations and derivatives. It should be possible for the user to
view a math expression as a separate item and enlarge it.

Priority: Should-have

#### The user could be able to change the capitalization of text to sentence style

Text written in all capital letters or all small capital letters is more
difficult to read for most people, with and without disabilities. Users
could have the option to choose a sentence-style version. Acronyms that
are correctly marked as abbreviations will remain in uppercase;
otherwise, they will be converted to sentence style. Users could also
be able to toggle between the different styles as needed.

Priority: Could-have

#### The user could be able to view the content in a paginated view

Many users prefer scrolling, while others like pagination. The user
could be able to use a paginated reading mode.

Priority: Could-have

#### The user could be able display mathematical expressions without color formatting, using a consistent text color instead

Sometimes, specific sections of mathematical expressions are highlighted 
in distinct colors. For some people this can present problems. The user 
could be able to remove the color formatting used in math expressions, 
so the chosen text color is always used.

Priority: Could-have

### Clarifying Note on Bookmarks, Notes and Highlights

Notes, bookmarks, and highlights are distinct features that support
different user needs in digital reading environments:

Notes are user-generated annotations that may contain text, audio, or
other formats. They are typically used to capture thoughts, questions,
or reflections on specific content.

Bookmarks are navigational markers that help users return to a specific
location in the content. They do not contain content themselves but may
optionally be enhanced with a note for added context.

Highlights visually mark portions of text to indicate importance or
relevance. They are often used for quick reference and may be used
independently or in combination with notes.

While these features can be used together---for example, attaching a
note to a highlight or a bookmark---they should remain functionally
distinct to support a wide range of user strategies and accessibility
needs.

### Bookmarking

The bookmarking features enable users to record their place in the 
content and return to it at a later point, which is particularly 
valuable in educational and reference contexts. The ability to create 
and manage multiple bookmarks is beneficial for all users. It is 
essential that this functionality be fully accessible to readers with 
print disabilities to ensure equitable use.

#### The user must be able to create bookmarks

The application must allow the user to set a bookmark at any arbitrary 
position within the content, whether being read in text or audio format. 
The application must allow the user to create and store multiple 
bookmarks within a single title.

Priority: Must-have

#### The user must be able to delete bookmarks

The application must allow the user to delete bookmarks individually 
within a title. The application could provide the option to delete all 
bookmarks within a title in a single action.

Priority: Must-have

#### The user must be able to view an overview of all bookmarks and navigate from there

The application must provide an overview of bookmarks sorted by their 
order of appearance in the book. This overview should be presented in a 
clear and navigable list, enabling users to identify bookmarked 
positions, select a bookmark to navigate directly to that point in the 
content. The application could allow the user to jump directly between 
bookmarks without going via the overview.

Priority: Must-have

#### The user must be able to identify each bookmark

The user must be able to identify each bookmark through a 
system-generated title that is both meaningful and distinguishable from 
other bookmarks.

The application should allow users to edit or rename system-generated 
bookmark titles to better reflect their personal context or preferences.

Priority: Must-have

#### Users should have access to their bookmarks if they open their book on another device

Users should have access to their bookmarks when opening the same book 
on another device, ensuring continuity.

Priority: Should-have

### Making Notes

The ability to add, review, and edit notes within a reading app is an
important feature for many users, especially those with print
disabilities or learning challenges. Notes provide a flexible way to
capture thoughts, highlight important information, or add personal
annotations, which can aid comprehension and retention. For users who
rely on assistive technologies, well-integrated note functionality (such
as easy navigation, and synchronization) ensures that these annotations
are accessible and usable across different contexts and devices.
Supporting notes alongside the text and/or the audio also enhances
interactivity and engagement with the content, making the reading
experience more personalized and effective.

#### The user must be able to create, review, edit and delete notes during reading

Users must be able to manage notes---adding, reviewing, editing, and
deleting them---while reading. Notes may be in text or audio format and
must be anchored to a specific location in the content (at least a text
range within a paragraph, or a timestamp). Visual indicators and screen
reader compatibility are essential to ensure discoverability and
usability for users with print disabilities.

Priority: Must-have

#### The user must be able to view notes in context, such as in a margin, overlay, or other adjacent display that maintains the user's reading position

Displaying notes together with the text improves usability and allows 
users to reference their annotations without losing their place in the 
reading material.

Priority: Must-have

#### Screen reader users must be able to navigate from one note to another

Efficient navigation between notes is essential for screen reader users
to manage and review annotations without losing context. This includes
the ability to move sequentially through notes, jump to specific notes,
and return to the reading position.

Priority: Must-have

#### The user must be able to save notes automatically, including during offline use

The user must be able to save notes automatically, including during 
offline use, to ensure no loss of information. When the device connects 
to the internet, notes must be synced. When the book is reopened, any 
notes saved during the last session should be automatically restored.

Priority: Must-have

#### The user should be able to apply basic formatting to the content of a note

Formatting options (bold, italic, and underline) allow users to
emphasize key points, structure their thoughts, and improve the clarity
of their notes. This can be especially helpful for users with cognitive
or learning disabilities who benefit from visual cues to organize
information.

Priority: Should-have

#### The user should be able to hide or show notes, either individually or all at once

Controlling the visibility of notes helps users manage visual complexity
and maintain focus, especially when reading for comprehension or
studying.

Priority: Should-have

#### The user should be able to have notes read aloud, either individually or all in sequence

Listening to notes supports users who rely on audio for comprehension or
who prefer auditory review. The ability to hear notes one at a time or
in sequence allows for flexible interaction with annotations.

Priority: Should-have

#### The user should be able to access their notes across multiple devices through synchronization

Synchronizing notes across devices allows users to continue reading and
working with their annotations without interruption. This is especially
important for users who rely on different assistive technologies on
different devices, or who move between environments such as home,
school, or work.

Priority: Should-have

#### The user should be able to export notes in a structured format

A straightforward way to share notes is by exporting them in a 
structured, non-proprietary file format. This exported file should 
include clear references to the text or timestamp the notes are anchored 
to, enabling recipients to understand the context. Users can then send 
this file to teachers, classmates, or others outside the reading system.

A more advanced option could allow users to share notes directly within
the reading system, enabling collaboration or review among users of the
same platform. This could include features such as real-time sharing,
commenting, or integrated feedback mechanisms.

Priority: Should-have

#### The user could organize notes using color coding or labels

Color coding or labeling helps users categorize notes in a way that
supports their reading goals, making it easier to locate and review
related information later.

Priority: Could-have

#### The user could be able to create notes in formats beyond plain text, such as handwriting, math notation, or video

Supporting multiple formats for notes allows users to record ideas in
ways that suit their needs and preferences. This flexibility is
especially valuable for users who find visual, symbolic, or spoken forms
more accessible than typed text.

Priority: Could-have

#### The user could attach notes to bookmarks

Check this isn't confusing things

Priority: Could-have

### Highlighting

Highlights allow users to mark important parts of the text for quick
reference. This supports efficient navigation and review, especially for
users who benefit from visual cues or who use highlighting as part of
their study or comprehension strategies.

#### The user must be able to create, review, edit and delete highlights

The user must be able to highlight any portion of the text, including 
partial sentences or individual words. The user must be able to remove 
or modify existing highlights easily. 

The application must ensure that highlights are saved automatically and 
persist across sessions, including offline use. Users should not need to 
take extra action to retain their highlights, ensuring continuity even 
when connectivity is intermittent.

Priority: Must-have

#### The user must be able to hide highlights

The user must be able to hide or show highlights at any time. This 
functionality should also be accessible to screen reader users, allowing 
them to read or navigate the text without interference from visual 
highlights while maintaining the ability to restore them when needed.

Priority: Must-have

#### The user must be able to change the color or category of highlights

The application must allow users to assign different colors or styles to 
highlights for categorization or emphasis. Both visually and through a 
screen reader, users must be able to distinguish between types of 
highlights to support study, reference, or personal organization.

Priority: Must-have

#### The user should be able to navigate from highlight to highlight

Users should be able to navigate quickly between highlights, for example 
via an overview list or table of highlights. The overview should provide 
context, such as the surrounding text or page location, allowing users 
to jump directly to specific highlights.

Priority: Should-have

#### The user could be able to annotate highlights

The application could allow highlights to include optional notes or 
annotations linked to the highlighted text. This would enable users to 
add personal comments or summaries while keeping them associated with 
the relevant passage.

#### The user could have their highlights synchronized across devices

Users could have their highlights synchronized across multiple devices 
for the same book. This would allow continuity of study or reading, 
enabling access to all highlights and annotations regardless of device.

Priority: Should-have

#### The user should be able to export highlighted sections

The application should allow users to export highlighted text, grouped 
by colors or categories where applicable. This would enable users to 
review, revise, or study key passages outside of the application, 
supporting learning and comprehension.

Priority: Should-have

### Entering Answers

**Special note:** reading systems typically let users add notes but
currently do not support answer entry. However, this is an important
need for learners with print disabilities. This section summarises user
needs for this functionality, based on workshops at Dedicon and
discussions with app developers and the user requirements working group.
This section aims to help designers and developers assess how this
functionality could be implemented.

Learners with print disabilities can face significant challenges when
completing exercises in books: if they are unable to read or write in
physical books, they are often required to write their answers into a
word processor, which can be time-consuming and mentally draining. The
ability to input answers precisely where questions or prompts appear in
the digital content makes the experience more intuitive and less
fragmented.

Questions can take many forms, and so the ability to enter various input
types---from simple text fields to multiple-choice selections---ensures
that all users can respond effectively and independently. Accessibility
features such as screen reader compatibility and the ability to save and
edit responses are essential for an inclusive and seamless user
experience. Additionally, synchronization and export options provide
greater flexibility, enabling users to access and manage their responses
across devices and contexts.

#### The user must be able to enter, edit and review answers into input fields embedded within a publication

The input fields must support a range of common types, including
single-line text fields, multi-line text areas, radio buttons,
checkboxes, and dropdown menus. This enables interaction with different
kinds of questions or prompts directly at the point where they appear in
the content, avoiding the need to switch to separate documents or tools.

Text input must be the primary format supported and could also
accommodate structured formats such as linear math (e.g., LaTeX or
Unicode math). Although audio input could be supported, it is not
anticipated to become the main method of interaction.

Priority: Must-have

#### The user must be able to save their answers

Saving should occur automatically to reduce the risk of data loss and to
support a seamless user experience. Ideally, answers are saved online to
allow synchronization across multiple devices. In such cases, the system
must also support offline use, with answers being stored locally and
synchronized once the device reconnects to the internet. If online
saving is not feasible, answers must still be saved locally in a
reliable and persistent manner.

Priority: Must-have

#### The user must be able to see previously saved answers when reopening a book

When a user returns to a publication, previously saved answers must be
restored to the input fields and clearly associated with their
corresponding questions or prompts. This ensures continuity in learning
and avoids the frustration of lost work. Restored answers must be
editable, so that users can continue working from where they left off.
This applies regardless of whether the answers were saved locally or
synchronized via an online service.

Priority: Must-have

#### Screen reader users must be able to navigate between input fields

Screen reader users must be able to navigate and review each question
and enter their answers using accessible controls, whether they are text
input (e.g., short or long text responses), checkboxes (for multiple
selections) or radio buttons (for single selections).

All input controls must be properly labelled, operable via keyboard, and
announced correctly by screen readers.

Priority: Must-have

#### The user should be able to format answers in text fields using a basic rich text editor

Some users, particularly in educational or professional contexts, may
need to emphasize parts of their answers using basic formatting options
such as bold, italic, or underline. This can help structure responses,
highlight key points, or mirror expected formatting conventions in
assignments. While implementing rich text editing in accessible reading
systems may present technical challenges, it is a feature users are
likely to expect in the future. Exploring this functionality now can
help prepare for more advanced input needs as digital reading systems
evolve.

Priority: Should-have

#### The user should be able to share answers with others (e.g. teachers, students)

A straightforward way to share answers is by exporting them in a
separate file format such as .html, .csv, or another accessible format.
This exported file should include clear references to the related
questions or assignments, enabling recipients to understand the context.
Users can then send this file to teachers, classmates, or others outside
the reading system.

A more advanced option would allow users to share answers directly
within the reading system, enabling collaboration or review among users
of the same platform. This could include features such as real-time
sharing, commenting, or integrated feedback mechanisms.

Priority: Should-have

#### The user could be able to add custom input fields where none exist

In some cases, content providers may unintentionally omit input fields
for certain questions or assignments within accessible publications.
Allowing users to add their own input fields ensures they can still
provide responses in these cases. These custom fields must support the
same range of input types as predefined fields, be fully accessible
through screen readers and keyboard navigation, and be included when
exporting answers.

Priority: Could-have

#### The user could be able to synchronize answers across multiple devices

This functionality applies only when answers are saved online. In such
cases, users' saved answers should be kept consistent across devices,
allowing them to seamlessly continue their work regardless of which
device they use. Synchronization must support offline use by storing
changes locally and updating them once the device reconnects. Secure and
reliable data transfer is essential to protect user privacy.

Priority: Could-have

#### The user could be able to have their answers automatically checked

Automatic checking of answers can provide immediate feedback to users,
helping them understand mistakes and improve their learning experience.
This feature may include validation of input formats, correctness of
responses, or basic grading where applicable. It should support a
variety of question types and be designed to complement, not replace,
human review and feedback.

Priority: Could-have

### Library and Bookshelf

Readers with print disabilities rely on a range of services, such as 
specialist online libraries, public and academic libraries, bookstores, 
and more—often using multiple sources. This section outlines user 
requirements for managing and accessing content within the reading 
application, whether the content is acquired through integration with 
online repositories or imported from other sources (e.g., sideloaded 
files). Some requirements apply specifically when the application 
integrates with one or more online catalogs, and their implementation 
may depend on the capabilities and interfaces those catalogs provide. 
Other requirements, such as managing the user's local bookshelf and 
accessing metadata for stored titles, apply regardless of such 
integration.

#### The user must have a simple way to log in to the reading system

Whether accessing titles through copyright exception, publisher
permissions, loaned from a library or purchased from a bookstore, users
will need to authenticate with the reading app. The user experience for
this must be accessible to users of assistive technology and the design
must take account of the needs and preferences of users with
disabilities. The authentication method can use up to date approaches
such as passkeys and biometrics but must avoid registration or
authentication interactions that create accessibility barriers. These
barriers could include inaccessible external websites, unreasonable
cognitive challenges, and CAPTCHAs that present barriers to assistive
technology or rely on visual matching.

Priority: Must-have

#### The user must be able to search, browse and acquire titles in a service provider's collection

To provide a comprehensive search, browse, and acquisition experience,
the reading app must enable users to search for titles within a service
provider's collection using keywords and advanced filters like genre,
publication date, language, and availability. Users should also be able
to browse the collection effectively through categories, curated lists,
and by author or series, with visual displays of book covers and
descriptions.

The app must facilitate title acquisition, allowing users to borrow
available titles, place holds, view purchase options, download content
for offline access, and manage their acquired titles within a dedicated
section.

To provide advanced search features an app could make use of an
accessible external website with additional capabilities for search,
filtering, etc.

If someone is making use of multiple catalogs the app could provide a
search across multiple collections (federated search).

Priority: Must-have

#### The user must be able to add titles from diverse sources

Users must be able to import (sideload) content into the app from
various external sources, such as titles obtained from other online
platforms or personal document files, ensuring they can seamlessly
access and read all their preferred content within the application.

Priority: Must-have

#### The user must have a simple way to subscribe to serial publications, and to end the subscription

The user must be able to effectively manage serial publications offered
by the service provider, such as newspapers, journals, and newsletters.
Users must be able to subscribe to and unsubscribe from these serials,
learn when new editions become available, and have the option to
automatically download new issues for immediate access.

Priority: Must-have

#### The user must be able to remove titles from their bookshelf

The user must be able to remove publications from their bookshelf. This
should effectively 'return' a title to the library when the service
provider operates such a model.

Priority: Must-have

#### The user must be able to download titles and read them offline

If the service model offers both download and streaming capabilities,
the user must be able to download a title, enabling them to read it
without requiring an internet connection.

Priority: Must-have

#### The user must be able to manage titles from multiple sources

The app\'s bookshelf must provide a cohesive and intuitive experience
for managing all user content, regardless of its origin. This means
seamlessly integrating titles downloaded from online libraries, serial
publications, and user-imported content.

Priority: Must-have

#### The user must be able to manage their diverse collection of reading materials

The bookshelf must enable users to browse through their collection with
ready access to key information about each title. This may be provided
in a grid or list format, with title covers displayed if they are
available. The user should be able to enlarge the title cover.

Users must be able to search their bookshelf by keywords, and sort and
filter their collection by various criteria such as author, title, and
date added, source, status, format, providing a highly personalized and
efficient way to navigate their diverse reading materials.

The app should offer a means of categorizing or tagging titles, ensuring
that users can more easily browse, access, and manage their diverse
collection of reading materials.

The user must be able to view more information about an individual
title, such as book metadata, format, duration, reading progress, and
accessibility features.

Priority: Must-have

#### The user's bookshelf must automatically reflect changes made in synchronized services

In the case where a library offers such a service, the app\'s bookshelf
must automatically synchronize with the user\'s online account(s). This
means any titles acquired or changes made on one device, or by a teacher
or administrator adding content to a user\'s account, this should be
reflected within the app\'s bookshelf across all the user\'s devices.

This requirement enables the possibility for a user to receive titles
from a provider without the need for the user to search the catalog and
download. The user must be notified of new titles when they are
automatically added.

Priority: Must-have

#### The user should be able to preview a publication when available

Users should be able to preview titles, whether they are browsing the
online collection or considering content already added to the bookshelf
in their app, when this is a feature that is offered by their library.
This functionality could extend to both audio and ebook titles, allowing
users to sample the content and determine if it suits their preferences.
For ebooks, this might involve a limited number of pages, while for
audiobooks, a short audio excerpt.

Priority: Should-have

#### The user should be able to open EPUB files directly from a file manager

Users should be able to tap an EPUB file in a folder or file manager and 
be presented with an option such as "Open in [App Name]", enabling a 
seamless and intuitive way to access content without needing to manually 
import it through the app interface.

Priority: Should-have

## Miscellaneous

#### The user must have user-friendly documentation

While the system should be intuitive, certain aspects like shortcut keys
still need to be clearly explained. The documentation should be concise
and user-friendly.

Priority: Must-have

#### The user must receive clear and user-friendly error messages

Users must be informed of any issues (e.g. failed uploads, missing 
metadata, unsupported formats) through concise, non-technical messages 
that explain what went wrong and how to resolve it. This ensures a 
smooth experience and reduces frustration when interacting with the 
application.

Priority: Should-have

#### The user must be able to access and read protected content using assistive technologies

Protected content---such as DRM-restricted publications---must remain
accessible to users with print disabilities. This includes compatibility
with assistive technologies like screen readers, braille displays, and
text-to-speech. While publishers may apply content protection to prevent
unauthorized use, these measures must not interfere with a user's legal
right to access content in an accessible format. Ensuring accessibility
of protected content is essential for equitable access to reading
materials.

Priority: Must-have

## Additional User Requirements for Future Consideration

This section includes user requirements that were identified as
potentially valuable but were not discussed in detail during the current
development cycle. Some of these ideas may be considered too
forward-looking for current implementation, while others were not
prioritized due to time constraints. They are included here to document
emerging needs and to support future exploration and innovation in
accessible digital reading.

#### Dynamic content based on user input (issue tracker #2)

The user could enter personal or contextual information (e.g., number of
servings, name, or variables) that dynamically updates the content of
the publication.

Allowing users to input values---such as the number of people to cook
for or a name for personalized narration---enables dynamic updates to
the content. This can make digital publications more engaging and
practical. For users with print disabilities, such features can reduce
cognitive load and improve usability by tailoring information to their
specific context. Similar use cases may apply to textbooks, where
variables or examples can be adapted to the learner's input.

#### Support for Tactile and Printable Content:

#### Print or Export Specific Content (issue tracker #3 and 5)

The user should be able to print selected parts of the publication, such
as templates or activity pages.

In interactive or instructional publications---such as handicraft books
or educational materials---users may need to print specific pages, like
templates or diagrams. Providing a way to print selected content
supports hands-on learning and accessibility for users who benefit from
physical or tactile formats. This feature may also support embossing or
other alternative output methods, depending on the user's needs and
available technology.

Additionally, limited printing or sharing of content from serial
publications---such as recipes or selected articles---could enhance
usability and encourage engagement.

#### Export Content for Alternative Format Production (issue tracker #5)

The user must be able to export content from the reading system in a
digital format suitable for creating alternative formats and supporting
materials.\
Priority: Must-have

#### Text Style Properties Must Be Exposed to Assistive Technologies (issue tracker #32)

If supported by platform accessibility APIs, text style properties such
as font, line spacing, indentation, justification, and emphasis (e.g.,
bold, italic, underline) must be exposed to assistive technologies.\
Priority: Should-have

Disclosing text style properties allows assistive technologies---such as
screen readers and braille displays---to convey visual structure and
emphasis in non-visual ways. For example, indentation and justification
can help represent layout on a braille device, while bold or italic text
may be rendered using specific braille indicators. This enhances
comprehension and preserves the author's intended structure and meaning
for users with print disabilities.

#### Turn hyphenation on/off (issue tracker #6 and 24)

Hyphenation can affect readability and comprehension, especially for
users with print disabilities such as dyslexia or low vision. Allowing
users to turn hyphenation on or off gives them control over how text is
presented, helping to reduce visual clutter and improve the flow of
reading. This customization supports a more accessible and comfortable
reading experience.

#### Synchronized Text-Audio and Switching between reading modes (issue tracker #7)

The functionality of synchronized text and audio---where professionally
narrated or pre-recorded audio is aligned with the visual text---is
already well represented in the Embedded Audio section of this document.
That section outlines key user requirements such as synchronized
playback, visual emphasis, navigation, and customization of the reading
experience.

However, one important aspect is not yet fully addressed: the ability
for users to switch flexibly between listening and reading modes. This
includes scenarios where a user may: Pause embedded audio to read the
text independently, either visually or with a screen reader; Resume
audio playback from the same point after reading; Transition seamlessly
between human narration, TTS read aloud, and screen reader use.

This kind of multimodal interaction supports diverse reading strategies
and is especially valuable for users with print disabilities who benefit
from combining auditory and visual input. Future development should
explore how reading systems can support synchronized state management
across different modes, ensuring continuity and user control regardless
of how the content is accessed.

#### Bookmarking (issue tracker #12)

Bookmarking is a widely used and valued feature in digital reading
systems. Although we did not have time to develop detailed user
requirements for bookmarks in this version of the list, we recognize
their importance for navigation, study, and personalization. Future work
should explore how bookmarking can best support users with print
disabilities, including possible integration with notes, accessibility
via assistive technologies, and synchronization across devices.

#### Follow external links (issue tracker #12)

Some digital publications include hyperlinks to external web resources.
Users should be able to follow these links and open them in an external
web browser outside the reading system. This supports access to
supplementary materials and ensures that users with print disabilities
can benefit from the full range of content referenced in the
publication.

#### Less distraction mode / Zen mode / Simplified interface (issue tracker #17 + 25)

A simplified or "Zen" mode could help users focus by hiding most
interface controls and presenting only essential playback or reading
functions. This can reduce cognitive load and visual distractions,
benefiting users with attention-related or cognitive disabilities. While
especially relevant for audiobooks, this mode could also support a
calmer, more accessible reading experience in text-based publications.

#### Reflow of text, for fixed layout as well (issue tracker #26)

#### Disclose test style properties to assistive technologies, e.g. for presentation braille device (issue tracker #32)

#### Support for LLM inference or other processing (issue tracker #33)

#### Support for parallel text viewing and navigation for linked content, such as translations or annotations (issue tracker #36)

#### Tactile graphics support (issue tracker #37)

#### Display word counts in tables of contents of serial publications

#### Digital clippings archive

#### Book recommendations based on personal preferences

#### Book recommendation sharing

#### Borrowing history indicator

:::
::: {#userstories .section}

## User Stories

The [user
stories](https://daisy.github.io/reading-apps-ux-reqs/use-cases/)
referenced in this document were developed by the working group.

:::
::: {#acknowledgments .section}

## Acknowledgements

This project would not have been possible without the contributions of
the DAISY members and Friends who participated in the project. Their
valuable insights, expertise, and experiences have been instrumental in
ensuring that the requirements capture a broad range of user needs.

This work is financially supported by [Dedicon](https://dedicon.nl).

:::
::: {#references .section}

## References

The [EPUB test: Latest test books](https://www.epubtest.org/test-books)
has many well-established fundamental accessibility tests which were
extracted and adapted for this document. The titles are:

1.  [Fundamental Accessibility Tests: Basic
    Functionality](https://www.epubtest.org/test-books/basic-functionality)
2.  [Fundamental Accessibility Tests: Non-Visual
    Reading](https://www.epubtest.org/test-books/non-visual-reading).
3.  [Fundamental Accessibility Tests: Visual
    Adjustments](https://www.epubtest.org/test-books/visual-adjustments)
4.  [Fundamental Accessibility Tests: Read
    Aloud](https://www.epubtest.org/test-books/read-aloud)

:::

</body>
</html>