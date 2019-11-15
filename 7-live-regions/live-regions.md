# Live Regions

## General

Live regions are areas of the page that can have dynamic changes where content will change, be inserted, or removed from the DOM. Those are more apparent to those who can see those changes obviously, so we need to make sure those are read to people who are using a screen reader.

**Rules:**

- Live region must first be present (and usually empty), so the browser/assistive technologies are aware of it.
- Additional changes to the live region will be announced.
- Distinct attributes can be used to define the screen reader behavior for live regions or specialized roles may be used for more common cases.

### ARIA Attributes
`aria-live` - defines the update priority when the screen reader reads updates to the region
  - `off` - default setting, won't read updates to region
  - `polite` - wait to read updates to the region once its idle
  - `assertive` - the screen reader will interrupt whatever its reading to read updates to the region
`aria-atomic` - `true` or `false` as to whterher


### Specialized Roles
`status` - status bar to provide updated status
`alert` - one thing to draw the attention to the user
`progressbar` - to show the user the progress of an upload, can give `aria-valuemin`, `aria-valuenow`, and `aria-valuemax`
`marquee` - used for scrolling text (stock ticker)
`timer` - countdown/stopwatch timer
`log` - chat, error, game, or other types of logs

VoiceOver can read us errors in our site. We can listen in for repetitions, or values that are missing from it to help debug.

`assertive` can interrupt the VoiceOver itself, so be wary when using. `polite` is generally a safer option for aria attributes that can help read errors.
