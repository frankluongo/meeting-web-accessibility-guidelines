# Section 1: Choosing a Web Conformance Guideline
-----------------------------------------------------------------------------------------

## Section 508
Reference: www.section508.gov
- quick reference guide

## WCAG 2.0
POUR = Perceivable / Operable / Understandable / Robust
Perceivable = everyone should be able to see it
Operable - Everyone should be able to operate it
Understandable - Users must be able to understand the information
Robust - Users must be able to use the technology

A, AA, AAA levels of conformance
A = Basic level
AA = Medium
AAA = Highest
Reference: https://www.w3.org/WAI/intro/wcag.php

## Section 508 vs. WCAG 2.0
WCAG 2.0 Level AA should be the goal
- WCAG is international
- This will also cover section 508


# Section 2: HTML
-----------------------------------------------------------------------------------------
## Document Structure and Landmarks
- Set <!doctype>, language and encoding
- Text resizing via viewport and relative units
- Unique Page <title>
- Landmarks
- Headings <h1> through <h6>

## Lists
List Types:
- Ordered List <ol>
- Unorded List <ul>
- Description List <dl />

Lists add semantic usability to a website
Screen readers can go through them easily
This meets level A 1.3.1 for WCAG
Visual cues, via CSS, must be conveyed non-visually via semantics

## Navigation and Skip Links
Consistent Navigation
Multiple Ways to Find Page / Content
Meaningful Link Content
Consistent Overall Interface
Skip Links

- Navigation should always be in the same order
- Add a Sitemap for usability and SEO

## Tables
Used for displaying content in rows and columns
Not useful for layouts
- Make tables as flat as possible

Parts of a Table
- <caption></caption> = Used to display text for the table
- <thead>, <tfoot>, <tbody> = Used for holding content
- <th>
- Scope and headers

## Forms

- Accessible Forms
- Error Identification
- Color
- Keyboard Nav / Focus

### Level AA 1.4.3 - Contrast
The visual presenation of text and images of text has a contrast ratio of at least 4.5:1


### Additional Guidelines
Level AA 3.3.4 Error Prevention
- Anytime a user is engaging in a legal commitment or financial transaction, they have to have the ability to modify, change, or delete that info. They can also review that info before submitting
Level 2.2.1 Timing Adjustable
- For each time limit that is set by the content, the user is able to either turn off, adjust or extend that limit


# Section 3: Media
-----------------------------------------------------------------------------------------

## Images
- Use real text instead of images of text

- All Images must use the Alt Attribute!
  `<img src="" alt="whatever">`
  - Images used for decoration should just contain an empty alt attribute, as screen readers will know to ignore them

### Tips for Writing ALT Text
- Don't describe the image literally
- Avoid using words like picture or image of
- Describe the meaning or purpose of the image
- Include any text used in the image

## Background Images Via CSS
- Use visually hidden spans to communicate the meaning of a background image

## SVG
- Add a `role=img` for semantics
- Use the `<title>` tag to describe it. This will be nested in the SVG
- Use the `<desc>` tag if necessary for a more descriptive explanation
- Add `aria-labelledby` that references the title tag
- Add `aria-describedby` to reference the desc tag if necessary

## Audio
### Create a transcript
  - Pay a service
  - Use speech recognition server
    - Google Docs Voice Typing
    - Window Speech Recognition
    - Apple Dictation
    - Dragon Naturally Speaking
  - Manual
  - Tips
    - Include names of speakers
    - Describe everything
  - You can provide these transcripts as a link or inline

## Video
  - Provide Captions
    - Types of Caption
      - Open Captions = Always visible, embedded/burned into videos
      - Closed Captions = Overlay, toggled on/off by the user
  - Captioning Prerecorded Video
    - YouTube
      - Auto-Subtitle
      - Upload a transcript and sync
      - Manual Entry
    - Video Captioning Services
    - Manual
  - Provide Audio Description
    - Narrate Non-Visual Cues

## Additional Media Guidelines
  - If any media is autoplayed, it should be able to be turned off if it's longer than 3 seconds
  - Content like carousel should be able to be paused
  - No more than 3 flashes per second
  - Any `<iframe>` embedded on a page should have a descriptive Title Attribute

# Section 4: Responsive Web Design & Accessibility
-----------------------------------------------------------------------------------------

## Switching Context
  - Whenever the page context changes, i.e. when a site navigation switches from a list of links to a dropdown, the user must be notified
  - The solution here is to use a hamburger menu to allow users to select where they want to go

## Order of Content / Focus
  - Visual order must match the DOM order because Screen readers depend on DOM order
  - Focus also has to happen in a logical manner
  - Autofocus should only be used when you have only one form, like Google
  - Focus should not move automatically from one field to another

## Additional Responsive Guidelines
