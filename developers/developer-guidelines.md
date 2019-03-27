# Developer Guidelines

<!-- TOC depthFrom:1 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [Developer Guidelines](#developer-guidelines)
	- [1. Build solid foundations](#1-build-solid-foundations)
		- [1.1. HTML must validate](#11-html-must-validate)
			- [Takeaways](#takeaways)
		- [1.2. HTML must be semantic](#12-html-must-be-semantic)
			- [Takeaways](#takeaways)
			- [Dive deeper](#dive-deeper)
		- [1.3. URLs must be used properly](#13-urls-must-be-used-properly)
			- [Takeaways](#takeaways)
	- [2.  Build usable User Interfaces (UIs)](#2-build-usable-user-interfaces-uis)
		- [2.1. Links must make sense](#21-links-must-make-sense)
			- [Material Honesty](#material-honesty)
			- [Usability](#usability)
			- [Did you know?](#did-you-know)
			- [Questions? What ifs?](#questions-what-ifs)
		- [2.2. Buttons must be usable](#22-buttons-must-be-usable)
			- [Material honesty](#material-honesty)
			- [Usability](#usability)
		- [2.3. Forms must be functional](#23-forms-must-be-functional)
		- [2.4. Images & media must be perceivable](#24-images-media-must-be-perceivable)
		- [2.5. Iconography must be clear](#25-iconography-must-be-clear)

<!-- /TOC -->

## 1. Build solid foundations

Building a solid, bullet-proof web application that is usable should be at the core of every developer's mindset from the very beginning of development.

**Otherwise...**
- If it is not solid or bullet-proof, it will break easily.
- If it does not function for some people, it is broken for all.

The key to building solid, bullet-proof web pages and applications is a solid foundation—which is HTML. The reason HTML is still the foundation of the web is because it is descriptive, simple to implement, and tolerant of input—making it incredibly stable as well as future-proof and backward compatible.

> "Be liberal in what you require but conservative in what you do."
> — Tim Berners-Lee, [Principles of Design](https://www.w3.org/DesignIssues/Principles.html#PLP)

### 1.1. HTML must validate

Use valid HTML5 markup.

While HTML linters and validator tools are a good start, you must always, double-check (i.e. Inspect) the DOM in your web page or web application to ensure the integrity of the HTML you expected. This includes knowing how to nest lists properly, how to mark up tables correctly, and general [block-level](https://developer.mozilla.org/en-US/docs/Web/HTML/Block-level_elements) and [inline element](https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements) rules (like not putting a `<div>` inside a `<span>`).

#### Takeaways
- Must write valid HTML5 markup. <!DOCTYPE html>
- Must utilize HTML validators and linters as a preliminary, sanity check.
- Must double-check (i.e. Inspect) the DOM to ensure the integrity of your HTML.
- Learn the difference between block-level and inline elements.

### 1.2. HTML must be semantic

Be intentional with your markup. Semantic HTML is naturally accessible.

In order to create usable web pages and applications, it is essential that every developer writes well-thought-out, semantic HTML. This requires a firm understanding of HTML5 and its proper use beyond the typical and generic `<div>` and `<span>` elements.

#### Takeaways

- Be intentional with HTML5's new semantic elements.
- Think about "what is this content?" rather than "how do I want it look?"
- Don't use `<div>` or `<span>` elements simply out of convenience.


#### Dive deeper

- [HTML is descriptive](descriptive-html.md)
- [HTML is naturally accessible](accessible-html.md)
- [Utilize Progressive Enhancements](progressive-enhancements.md)
- [Don't Misuse HTML](bad-html.md)
- [Avoid deprecated or obsolete HTML elements](obsolete-html.md)

### 1.3. URLs must be used properly

URLs (or URIs) are one of the foundations of the web—[the glue that binds the web](https://www.w3.org/2004/11/uri-iri-pressrelease) together in fact. For this reason, we must follow a set of best practices (or Web Standards) to ensure our web pages and web applications function according to users' expectations as well as providing users with stable, accessible experiences.

#### Takeaways

-   URLs should be human-readable.
-   Avoid exposed query strings, cryptic numbers, and file extensions (where possible, like `.html`, `.php`, etc.).
-   Separate words with hyphens (dashes) not underscores.
-   Special characters must be encoded in URLs.
-   Any page, app "page", or [resource of significance](https://www.w3.org/DesignIssues/Axioms.html#Universality) should be given a URL.
-   Do not return [differing information](https://www.w3.org/DesignIssues/Axioms.html#abuse) under the same URL.
-   [Provide Clean URLs](https://webmasters.googleblog.com/2016/11/building-indexable-progressive-web-apps.html) by using Fragment Identifiers (i.e. hashes) responsibly.
-   Avoid using Fragment Identifiers for saving client-side "history" within JavaScript frameworks (e.g. `#user/24601/` or `#!user/24601/`).
-   Utilize the History API (e.g. pushState) in single page apps.
-   *Try* to use Progressive Enhancement methodology to ensure URLs work with and without JavaScript.

## 2.  Build usable User Interfaces (UIs)

### 2.1. Links must make sense

#### Material Honesty

-   Only use hyperlinks (`<a href>`) for linking to additional content or pages.
-   Be honest about what is a button and what is a link.
	- Make links look like links.
	- Make buttons look like buttons.
-   Avoid using blue for non-links. Do your best to ensure that only clickable/actionable items are blue.
-   Don't be misleading in hyperlink text. Always link to a relevant content page.

#### Usability

-  [Don't use "click here"](https://medium.com/@heyoka/dont-use-click-here-f32f445d1021) or other vague, non-descriptive hyperlink text.
-   Write clear and concise hyperlink text.
-   Don't use "learn more" as a call-to-action. It is better to link a heading.
-   Do not use the same hyperlink text for different URLs. Doing so would be confusing to a user (e.g. "learn more"). Use the same URL destination for the same link text.
-   Do not use a URL as the hyperlink text, unless the use of the URL is concise (like redhat.com) and necessary for the user to remember the URL.
-   When linking to something that is not a web page (like a PDF), you must indicate the file/format with text or an ARIA label (not just an icon). *Read next bullet point too.*
-   Always provide text or a proper text alternative for icons or visual elements (like arrows) that are essential to the UI.
-   Do not rely solely on color to convey meaning.

#### Did you know?

- Title attributes are not sufficient as an alternative to text. You must provide screen reader only text or an ARIA label.
- Links in a list are easier to perceive than links embedded in a paragraph.

#### Questions? What ifs?
Please read [hyperlink tips and tricks](hyperlink-tips-tricks.md).

### 2.2. Buttons must be usable

#### Material honesty

-   Be honest about what is a hyperlink and what is an actual button (element). They have different meanings as well as operation.
	- Make links look like links.
	- Make buttons look like buttons.
-   Avoid using other elements, like `<span>` or `<div>`, for buttons.
	- If it is unavoidable, make sure to properly manage the user's focus (`tabindex="0"`).
-   Avoid using blue for non-buttons. Do your best to ensure that only clickable/actionable items are blue.

#### Usability

-    [Don't use "click here"](https://medium.com/@heyoka/dont-use-click-here-f32f445d1021) or other vague, non-descriptive button text.
-   Write clear and concise button text.
-   Always provide text or a proper text alternative for icons or visual elements (like arrows) that are essential to the UI.
	- If your button just has an icon, make sure it has an `aria-label` or screen reader only text.
-   Do not rely solely on color to convey meaning.

### 2.3. Forms must be functional

-   Every `<input>` should have a `<label>`, referenced with "id" and "for" respectively.
-   Provide clear feedback for form errors.

### 2.4. Images & media must be perceivable

-   Must have alternative text that describes images or non-visual media (like captions and video transcripts) that are perceivable in the DOM (not embedded).
-   Don’t use images to replace text—prefer text over images wherever possible. Also helps with page speed.

### 2.5. Iconography must be clear

-   Don’t solely rely on visual indicators.
-   If the icon is more than simply presentation, always provide text or a proper text alternative, like an ARIA label.
