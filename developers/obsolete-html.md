# Avoid deprecated or obsolete HTML elements

Developers should do their best to avoid [deprecated or obsolete](https://developer.mozilla.org/en-US/docs/Web/HTML/Element#Obsolete_and_deprecated_elements) HTML elements.

At the start of HTML4, many elements that once had "visual meaning," like [`<font>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/font) or [`<center>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/center), have since been marked as obsolete. Other elements, like the [`<iframe>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe#Accessibility_concerns) element, should be avoided because they could be confusing for all users—whether sighted or visually impaired. The [`<frame>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/frame) and [`<frameset>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/frameset) elements are both extremely confusing for users as well as obsolete.


Image maps ([`<map>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/map), `<area>`, `usemap`) should also be avoided due to [unreliable implementations](https://www.w3.org/WAI/tutorials/images/imagemap/) across browsers, on mobile devices, and with assistive technologies.

## Takeaways

- Do not use [deprecated and obsolete elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Element#Obsolete_and_deprecated_elements).
- Avoid `<font>`, `<center>`, and other elements with "visual meaning."
- Avoid `<iframe>`, `<frame>` and `<frameset>` elements, since they're confusing for users.
- Avoid image maps ([`<map>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/map)) because they’re unreliable.
