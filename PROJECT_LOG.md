# Project Conversation and Decision Log

## Purpose

A simple website the user can share with friends to invite them to a dinner party.

## Conversation summary

### 2026-10-27

- The user asked to create a new project, connect it to a separate GitHub repository, and keep conversation summaries and decisions in this Markdown file.
- The user wants to discuss the design before implementation and explicitly said not to write code yet.
- The project is a simple dinner party event page for inviting friends.
- The user does not want unsolicited initial tool ideas.

## Decisions

- Project concept: a dinner party invitation website.
- Repository: the separate public repository `mna2145-cloud/dinner-party-invitation`.
- The user asked for an initial HTML pass, followed by a simple CSS pass. JavaScript behavior has not been requested.

## Implementation progress

- Created an initial HTML page structure in `index.html` based on the agreed outline. The RSVP button does not submit.
- Added `style.css` and linked it from the HTML. The page uses a light pink background, dark green text and borders, and simple outlined blocks around the header, content sections, and footer.
- Chose Trebuchet MS with a sans-serif fallback for the page font.

## Design discussion

- A basic page outline was agreed before implementation and is preserved below.
- The RSVP area should include fields for a guest’s name and dietary restrictions next to the RSVP button.
- Event details and final invitation copy remain undecided. The visual style is a light pink background with dark green text and outlines, using Trebuchet MS. RSVP fields and a button are present as a static visual prototype; no submission behavior is implemented.

## Open questions

- What event details should appear (date, time, location, dress code, menu, host/contact)?
- How should RSVP submission be handled if JavaScript is added later?
- What visual style should the invitation use?

## HTML learning notes

The user asked these questions while reviewing `index.html`:

- **What does line 43 mean?** `<section aria-labelledby="rsvp-heading">` starts the RSVP section. The `aria-labelledby` attribute associates the section with its heading (`id="rsvp-heading"`) so assistive technologies can identify the section by name.
- **What is the difference between `<div>` and `<section>`?** `<section>` marks a distinct, topic-based part of a page, usually with a heading. `<div>` is a generic container without semantic meaning, often used to group elements for layout or styling.
- **What does line 47 mean?** `<form>` begins the group of RSVP controls. It does not specify a submission destination by itself. The current button is `type="button"`, so clicking it does not submit the form; the inputs are only part of the visual prototype.
- **Why is the form outside of the div?** The form wraps all RSVP fields and the button. Each `<div>` groups one label and its input. This keeps the two field groups separate while including both in the same form.

## Agreed ASCII mockup

This is the latest text outline discussed before implementation. Bracketed content is placeholder copy; RSVP is a visual prototype and does not submit.

```text
┌─────────────────────────────────────────────────────────┐
│                                                         │
│                     YOU'RE INVITED                      │
│                                                         │
│                  [Dinner Party Title]                   │
│                                                         │
│          An evening of good food and good company       │
│                                                         │
│                   [Date] · [Time]                       │
│                   [Location]                            │
│                                                         │
│             [Optional short invitation note]            │
│                                                         │
├─────────────────────────────────────────────────────────┤
│                                                         │
│   THE EVENING                                           │
│   [A few words about the plan, menu, or occasion]        │
│                                                         │
│   WHEN                       WHERE                      │
│   [Date and time]            [Address or location]      │
│                                                         │
│   WHAT TO KNOW                                          │
│   [Dress code, what to bring, dietary notes, etc.]       │
│                                                         │
│   RSVP                                                  │
│   YOUR NAME             DIETARY RESTRICTIONS             │
│   [______________]      [________________________]      │
│                                        [RSVP button]     │
│                                                         │
│               Hosted by [Your Name]                     │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

## GitHub publishing

- The user requested publishing the current version to a separate GitHub repository.
- Connection check on 2026-10-27 confirmed that the GitHub integration can access the account.
- On 2026-10-27, created the separate repository `mna2145-cloud/dinner-party-invitation` and published `index.html`, `style.css`, and this project log to its `main` branch. The user later confirmed changing it from private to public.
