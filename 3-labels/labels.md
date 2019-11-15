# Labels

## General

We want clear labels and descriptions when building our layouts to add context and clarity for screen readers.

There may be times a designer asks you to do things a certain way, but it's not fully there. When you're able to make that small tweak you see to make it better, you have to iterate on those things.

**Flow:** Interpret the experience -> ask what tweaks can make it better -> make those changes.

### aria-label

Use `<label>` element for labeling `<input>` elements. To do so, wrap the `<input>` that's being labeled, or use the `htmlFor` attribute with the id of the `<input>` being labeled.

We use `aria-label` where a text label is not visible on the screen.

When we don't supply the prop (assigning it with null), React will simply exclude it. It's a good way to have optional things for no unnecessary junk.
- In addition, we can be more verbose with the `aria-label` we aren't supplying directly to the screen, as the user listening could be more informed without us losing the efficiency of screen space

### aria-labelledby

We use `aria-labelledby` when there is visible text labeling the element, as opposed to `aria-label` which is when a text label isn't visible.

### aria-describedby

It works the same as `aria-labelledby` in that you provide ID's that are already provided on the page, but its intention is really more for providing:
- instructions
- important usage details

If you see you have an `aria-labelledby` that you can make the change to an `aria-describedby`, then do so. They function nearly the same.

## User Questions

Nick V: *How do these labels intersect with localization? Have you used those together with React international?*
- Yes I have, if you are using React International or whatever you have, you want to _translate the text_, _get the result_ (translated text result), then depending on what label you are using, _pass it in that_.
