
# Don't Misuse HTML

Never misuse HTML5 elements. If you are unsure of the meaning of an element, [look it up](https://developer.mozilla.org/en-US/) before assuming.

In addition, take caution when using "[changed elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/hr)" (e.g. `<hr>`), and use them properly or avoid them altogether if you are unsure of their proper use. To be used properly, these elements must be used according to their new semantics in HTML5, like `<i>` or `<b>`.

**For example:**
-   `<hr>` now means "thematic break" not "horizontal rule", and should be avoided altogether to prevent confusion—it would be better to use the more semantic `<section>` element.
-   `<br>` should be avoided unless using it explicitly for a literal line break like in a post address. Never use a `<br>` for visual spacing (that's what CSS is for).

## Common, semantic implementations

### Clickable buttons

#### Correct Implementation

```html
<button>Button Text</button>
```

#### Incorrect Implementation(s)

```html
<a>Button Text</a>
<a onclick="...">Button Text</a>
<span ng-click="...">Button Text</span>
<div>Button Text</div>
```
Remember, HTML is for semantics, CSS is for styling. If you don't like the way a `<button>` looks, use CSS to change its appearance.

### Links

#### Correct Implementation

```html
<a href="...">Link Text</a>
```

#### Incorrect Implementation(s)

```html
<a onclick="...">Link Text</a>
```

#### Did you know?

An anchor (`<a>`) tag without an `href` attribute or `tabindex="0"` is not focusable, and therefore it is inaccessible. Moreover, using only a `tabindex` in lieu of an `href` would be an anti-pattern because of its [material dishonesty](https://medium.com/simple-human/but-sometimes-links-look-like-buttons-and-buttons-look-like-links-9b371c57b3d2)—a false affordance to some users.

*Remember: Make buttons buttons and links links.*

### Text that’s intended to be visually smaller


#### Correct Implementation

##### HTML
```html
<span class=”exampleClass”>Lorem ipsum dolar</span>
```
##### CSS
```css
.exampleClass {
  font-size: 0.75em;
}
```

#### Incorrect Implementation(s)

```html
<small>Lorem ipsum dolar</small>
```

#### Did you know?

In HTML5, [`<small>` tags](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/small) are only for side comments and fine print, like copyright and legal text.

So, don't use `<small>` just to make text small. It doesn't *mean* that.

## Takeaways

- Do not misuse HTML5 elements.
- Never assume the meaning of an HTML element.
- If you’re not 100% sure of an element’s purpose or meaning, look it up!
- Avoid changed elements, like `<hr>`.
- Never use tables for layout.
- Only use anchor links (`<a>`) for links. **Do not** use them for buttons.
