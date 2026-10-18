## Task [4 B] — [Technique]
**Objective:**
Explore how examples and specialized perspectives influence AI output.
**Exact Prompt:**
> [Act as a frontend accessibility reviewer. Examine my generated Tourism and Cultural Innovation in Marinduque website. Identify problems involving HTML semantics, keyboard access, labels, and visual clarity. Recommend targeted improvements without changing the project's scope. Check whether the navigation links and buttons are accessible using a keyboard, whether the headings and sections use appropriate semantic HTML, and whether the text and layout remain readable on mobile screens. Identify the two most important issues based on the actual source code. Recommend specific corrections and explain how I can test them. Do not rewrite the entire website or add new features. Keep the project limited to a single-page website using HTML, CSS, and vanilla JavaScript.]
**Actual Copilot Output:**
[Top two accessibility issues
Mobile navigation can hide the keyboard focus after a link is activated.
The menu button has a name, aria-expanded, and aria-controls, and the links are keyboard-operable. Escape also closes the menu and restores focus. But when a navigation link is activated, script.js closes the menu without moving focus. On mobile, the focused link is then hidden by display: none in styles.css.
Recommendation: When a mobile navigation link is activated, close the menu and return focus to the visible Menu button—or move focus to the destination. If returning focus to the button, do so only at mobile widths, since that button is hidden on desktop.
Test: Using only the keyboard on a phone-sized viewport, Tab to Menu, press Enter or Space to open it, then activate each link. Confirm the destination scrolls into view and keyboard focus remains visible. Also check that Escape closes the menu and restores focus.

Some text is very small, especially photo credits and category labels.
Photo captions are 9px, category labels 10px, and card descriptions 13px in styles.css. The layout switches to one column on mobile, which helps, but the smallest text may still be difficult to read.
Recommendation: Increase photo credits to at least 11–12px, category labels to 12px, and card descriptions to 14–16px; keep enough line-height for wrapped text.
Test: Check at 320–390px viewport widths and 200% browser zoom. Confirm captions, labels, and descriptions are readable without horizontal scrolling.

Other checks
The page has a sensible heading hierarchy (h1, h2, then card h3s), a labeled navigation landmark, semantic main, section, article, and figure elements, and descriptive image alt text. The menu and back-to-top control are buttons, and visible keyboard-focus styling is defined. I reviewed the source and have not changed the files.]
**What Worked:**
Copilot produced 6 consistent cards with a good mix of destinations, culture and sustainable tourism ideas, namely the following: Name, Category, Description. These are all responsive cards and the Culture and Innovation links lead to the appropriate cards.
**What Needs Improvement:**
 The output contains a typo in it (“based on for examples”) and there is no evidence that it verified the photos and links. The images are also still reliant on external links.
**Next Action / Verification:**
Correct the typo and re-run the prompt, then verify that all cards are congruent, images load, and the format remains readable on phone and tablet.