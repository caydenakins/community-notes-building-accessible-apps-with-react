# Color Contrast

## General

We need to increase the ratio for color contrast when the contrast between the foreground and background colors is not sufficient enough, making it hard to distinguish outlines, borders, text, and the like.

The ideal ratio is 4.5:1. These numbers were chosen because they compensate for the greatest loss in the contrast under most backgrounds and other circumstances.

We shouldn't use color alone to convey meaning. If we want to show something is an error and we change the color from green to red, it can end up being missed by people who have issues with color contrast or color blindness. We have to add more to our design to convey these different meanings.
- To better convey these messages, we should use:
  - typography
  - shapes
  - grids
  - spaces
  - borders
  - extra weight

Using high contrast mode can help you find these inconsistencies. Remember: `Windows High Contrast Mode` differs from the Chrome extension `High Contrast`

**Detection:**

- Axe can help us detect these things and give an error message: `Text elements must have sufficient color contrast against the background`.

- Totally will give you examples of what would be a better contrast example, as well letting you preview those.

- Chrome dev tools in `Styles` will also actually tell you which WCAG (Web Content Accessibility Guidelines) level it's not meeting, as well as the ratio it needs to be to meet that level.

[color.review](https://color.review/) is a helpful tool where you can grab your hex values for your app and plug them in. It'll show you the lines that you need to cross to meet those standards.
