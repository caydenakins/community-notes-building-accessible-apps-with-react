# Landmark Regions

VoiceOver gives users a map of the page, letting them jump to specific things/sections they want to go to.

If you are running Windows, it is highly recommended to run the default `High Contrast Mode` that comes with your system, as well as the `High Contrast` Google Chrome extension to test your site. These help you find inconsistencies in your site and assure all users can view your page.

## General

Landmark regions is a way to define the structure of the page so users can navigate to the content they want to get to, typically using things like the rotor.

We can define landmark regions by `HTML5` elements or `ARIA` attributes.

`ARIA` vs `HTML5`: HTML elements are more semantic, but if you really need to use a div or other styling, it's not bad if you use ARIA.
- Note: there are certain role types some elements can't be applied to

The rotor is helpful because it can bring users to desired areas. The user can jump straight to the footer of the page if they want.

We can create lower level accessibility components with React.

Constantly think about how you can reuse things and the accessibility.

## User Questions

Daniele Tortora: *Is there reason why wrapping component into div instead of using fragment?*
- There is not a reason. If I remember correctly, when I first wrote and built this app, fragment wasn't as big of a deal. And it sort of since has been, so I started adding it in some places in the app, but I didn't add it in perfectly. **I do recommend using fragment over div if that div doesn't bring anything else to the table**.
