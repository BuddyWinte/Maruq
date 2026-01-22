# Maruq

**The modern, accessible replacement for `<marquee>`.**

> Maruq is currently **in Beta**. Please expect bugs, and please report those bugs (or suggestions) you have.

Maruq brings marquee-style scrolling back to the web using modern CSS and JavaScript — without deprecated HTML, while remaining lightweight, flexible, and CDN-friendly.

- Works with plain HTML
- Supports legacy `.maruq` divs
- Custom element support via `<maruq-element>`
- Framework-friendly (React, Vue, Svelte wrappers coming later)
- No dependencies
- Open source (MIT)

---

## CDN Usage (Recommended)

Maruq can be used directly from a CDN with **no build step**.

### jsDelivr (recommended)

```html
<link
  rel="stylesheet"
  href="https://cdn.jsdelivr.net/npm/maruq@0.0.9/dist/maruq.min.css"
/>
<script
  src="https://cdn.jsdelivr.net/npm/maruq@0.0.9/dist/maruq.min.js"
  defer
></script>
```

### unpkg

```html
<link
  rel="stylesheet"
  href="https://unpkg.com/maruq@0.0.9/dist/maruq.min.css"
/>
<script
  src="https://unpkg.com/maruq@0.0.9/dist/maruq.min.js"
  defer
></script>
```

---

# Basic Usage
Custom Element (Recommended)
```html
<maruq-element behavior="scroll" speed="30">
  <span>Hello world</span>
</maruq-element>
```

# Legacy / Plain HTML
```html
<div class="maruq" behavior="alternate" speed="20">
  <span>Scrolling content</span>
</div>
```
> Legacy / Plain HTML may not be supported in the future, but only time can tell. **For right now, please use __Custom Element__ if possible, if not, then you can use the `<div>` method.**

---

# Attributes
| Attribute          | Description                                 |
| ------------------ | ------------------------------------------- |
| `behavior`         | `scroll` (default), `slide`, or `alternate` |
| `speed`            | Duration in seconds                         |
| `bgcolor`          | Any valid CSS color                         |
| `pause-on-hover`   | Pauses animation on hover                   |
| `stop` / `stopped` | Prevents the marquee from running           |
| `loop`             | Number of loops (`0` or `-1` = infinite)    |

# JavaScript API
Each marquee element exposes simple methods:
```js
const el = document.querySelector("maruq-element");

el.start(); // start scrolling
el.stop();  // stop scrolling
```
### Events
- `start` - fired when scrolling starts
- `bounce` - fired when reaching an edge (alternate only)
- `finish` - fired when a finite loop completes

# Accessibility
Maruq respects user motion preferences:
- Automatically disables animation when `prefers-reduced-motion: reduce` is enabled

# License
MIT
