# Hyperlink Tips & Tricks

## Question: Can I use a "learn more" call-to-action?

**Answer: Please, don't.** You can do better.

### *Why? How so?*

Imagine you're a user who is blind. You've come to a new website, and you want to see what links are available. So you use one of your [shortcuts for links](https://webaim.org/resources/shortcuts/jaws#links) on the page. And, you hear something like this from your screen reader:

- Products, link.
- About us, link.
- Contact us, link.
- Click here, link.
- Learn more, link.
- Learn more, link.
- View more, link.

*Where do the last 4 links take you?*

But, the designer did such a good job laying out those "card" components with headings and "learn more" calls-to-action (CTAs) links below each, right? Visually, it's easy to associate each "learn more" with the heading above it, but therein lies the problem: "visually." We often take for granted our ability to quickly scan and make visual associations between elements in a layout.

For a user whose only reference to the information available is [haptic](https://en.wikipedia.org/wiki/Haptic_technology) or auditory, how would they know one "learn more, link" from the other?

**Quick answer: *they don't.***

### Instead, it is better to...

- Link a heading, rather than use a separate "learn more" link.
- Rephrase your CTA or link text so that it isn't vague on its own. For instance, "More about us", "View more news" or "Learn more about our products".

### If you *really* have no choice...

You can follow one of two more complicated routes using [ARIA](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA).

1. Apply an `aria-labelledby="associatedHeadingID linkID"` on the link so it can be properly associated. <br>For instance: `<h2 id="guachoHeadline">Gauchos Win Again</h2>`<br>`<p>The Gauchos have done it again!...</p>`<br>`<a href="/gauchos-win-again" id="guachoLink" aria-labelledby="guachoHeadline guachoLink">Read more</a>`<br>Will be spoken as: *"Gauchos Win Again, Read more, Link"*.

2. Or apply an `aria-label` to the link so it will change the spoken text (or "[accessible name](https://developer.paciellogroup.com/blog/2017/04/what-is-an-accessible-name/)") for the screen reader.<br>For instance: `<a href="/gauchos-win-again" aria-label="Gauchos Win Again, Read more">Read More</a>`<br>Will be spoken as: *"Gauchos Win Again, Read more, Link"*.

**But, there's an inherent problem with going this route.** ARIA patches this problem *only* for devices that utilize and understand ARIA. The root of the problem still remains: poorly constructed content that leaves a user with "[poor information scent](https://www.nngroup.com/articles/information-scent/)."

Users who may not have screen readers or devices that interpret ARIA could still find the "learn more" links disorienting due to [cognitive strain](https://www.nngroup.com/articles/learn-more-links/). For example, users with low vision who have zoomed into the content may not be able to easily associate the CTA with its heading. Or users with cognitive disabilities may have trouble making the association altogether. In fact, all users will experience an increase in cognitive load while they make the association between link and header anyway (whether they do so quickly or not). So why make the user experience worse to save a few words?

Instead, we should create clear and concise link text to improve information scent and reduce the cognitive strain for *all* users.
