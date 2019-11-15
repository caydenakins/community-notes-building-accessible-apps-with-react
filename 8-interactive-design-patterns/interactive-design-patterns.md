# Interactive Design Patterns

## General

At times when HTML falls short and custom 'widgets' are necessary, we can use complex menus, sliders, dialogs, tab panels, and more to support keyboard/screen reader accessibility.

The goal of changes in design pattern and toolbar is to give more context to someone using a screen reader.

- When we have more complex widgets, like combining various divs and aria attribute roles, there are expectations for how the widgets should behave and be navigated.

- Interactions must be intuitive and predictable.

- Events should be able to be triggered by mouse and keyboard, not just one or the other.

- The state of the widget should be clear.

## Expectations

### Tablist Design Pattern

Aria Roles:
- The element serving as the container for set of tabs has `role="setlist"`
- All elements serving as tabs have `role="tab"` and is contained within `role="setlist"`

Labeling:
- If tab has visible label, `role="tablist"` uses `aria-labelledby`, or will default to `aria-label`
- Each element with `role="tabpanel"` has the property `aria-labelledby` referring to its associative tab element

Attributes:
- Each element with `role="tab"` has the property `aria-controls` referring to its associated tabpanel element
- The active tab element has state `aria-selected` set to `true`, all other tab elements have it set to `false`

Keyboard Interaction:
- When focus moves into `tablist`, place focus on the active `tab` element
- When the `tablist` contains the focus, moves focus to next element in page tab sequence outside `tablist`
- `Left Arrow` - moves focus to the previous `tab`. If the first `tab`, moves focus to the last `tab`
- `Right Arrow` - moves focus to the next `tab`. If the last `tab` element, moves focus to the first `tab`
- `Space or Enter` - activates the `tab` if it was not activated automatically on focus
- `Home (Optional)` - moves focus to the first `tab`. Optionally, activates the newly focused `tab`
- `End (Optional)` - Moves focus to the last `tab`. Optionally, activates the newly focused `tab`

### Toolbar

The information extends further than just the toolbar. It should give information as to its location and what it is contained in.

A container for grouping a set of controls such as `buttons`, `menubuttons`, or `checkboxes`

- Use as a grouping element only when group contains 3 or more controls

Keyboard Interaction:
- Focus always starts on first control that is not disabled
- `Left Arrow` - moves focus to the previous control
- `Right Arrow` - moves focus to the next control
- `Home (Optional)` - moves focus to first element
- `End (Optional)` - moves focus to last element

## User Questions

Daniele Tortora: *What if I have content that has an animation once something is opened? How do I notify a screen reader of this?*
- I don't have much experience with this, but look at the live regions. You could notify the user of 'x amount of seconds left' or 'loading'.

Frances Jurek: *We are looking to raise awareness about accessibility (some don't catch everything like linting), we are thinking of adding some tools, knowing they don't catch anything are there any other tools you didn't demo today that you recommend?*
- You can use axe-core. Deque labs also has a lot of tools to add to your unit tests. ([axe-core](https://github.com/dequelabs/axe-core))
