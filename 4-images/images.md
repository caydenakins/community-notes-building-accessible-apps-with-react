# Images

## General

Images should have text alternatives that describe the information or function represented so they can be read and understood by those using screen readers.

**Note:**

All `<img>` elements should have an `alt` attribute provided.
- When not provided, many screen readers will fall back to reading the file name instead.

The `alt` value should not include words like 'image', 'picture', or 'icon'. Screen readers already announce the element is an image.

For images used to initiate actions rather than convey information (typically in buttons, links, and other interactive elements), use `alt` to convey the action that will be initiated, rather than a description of the image.

Images of text are not recommended, as it is better conveyed with actual text/CSS to give the design you want. However, if it's not possible, the `alt` should have all text in the picture.

Images that are decorative only and provide no information or function to the page should be hidden from assistive technologies by providing an empty `alt` attribute (`alt=""`). Make sure it's empty and doesn't include a text.

## User Questions

Daniele Tortora: *Is there a difference between having `alt=""` and `role="presentation"` on the image?*
- I'm not exactly sure how that works and if it's consistent across all screen readers... (cont.) so that might be something you need to look into.
  - _Learner's Advocate Note_ - They both have different uses/purposes. The `alt` attribute is only valid on image elements, whereas `role="presentation"` is essentially an empty alt attribute for all elements, not just images (however, it has less support than empty image alts). It's worth noting, another method is `aria-hidden="true"`, which is intended for elements and hidden to all users.
