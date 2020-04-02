# VHL Code Exercise

## Running The Project

> Using the NPM package will serve the page using http, allowing the use of
> auditing tools like Chrome's Lighthouse.

### Prerequisites
* Any version of Node from 2019 or newer.

### Setup
* Clone this repository to your computer.
* `$ npm install`
* `$ npm start`
* Visit `http://localhost:3000` in your browser.

## Approach

All of the code is located in `./jon-richards_vhl-menu-exercise.html`.  After
clarifying with VHL, it was clarified that stylistic precision wasn't the focus
of this particular exercise.  The most notable difference between the mockup and
the final html is the size of the menu.  The mockup appeared to be 108px/inch,
which is in-between Retina and standard pixel density.  I gathered measurements
from the mockup after down-scaling it to 72ppi, which appeared a little more
typical.  Colors were sampled via Photoshop's color picker.  The mockup was in
.PNG format, so its unlikely the colors are precise.

The CSS uses BEM naming conventions and is organized in a way that facilitates
componentization.  (This in contrast with declarative CSS, e.g. that used by
tools like Bootstrap and Tailwind, which is generally faster to get up and
running, but harder to change later on depending on how granular the declarative
classes are.)

Accessibility was a major topic during the interview process.  As such, I made
sure that the menu is keyboard accessible and that all elements carry semantic
meaning when used with a screen reader.  This was tested with Chrome's
Lighthouse auditing tool and Firefox's Accessibility tools.

Both tools raised warning about the contrast ratio between blue text and its
white background.  Fixing this would have been a large deviation from the
design, so I avoided it.  (Normally I would ask for input from the designer.)

I included a fourth menu item designed specifically to overload the topic
and subtopic fields.

## Takeaways

From a UX perspective, the menu is a bit "jumpy", especially due to the border
at the bottom of men items when focused.  I'd like to find a more elegant
solution to this.

Ideally, I would have sought more specific colors, fonts, and padding for the
sake of consistency.

The contrast ratio warning are unfortunate.  Ironically, the disabled option
(medium grey on light grey) doesn't throw a warning.  It would be great to get
a second opinion on this via QA or a consultant.