# HTTP observations (Lab 4, Task 1)
 
| Question | My answer |
|----------|-----------|
| Request method for index.html | GET |
| Status code with Disable cache ticked |200 |
| Status code on a normal reload | 304 |
| Status code for /nothing-here.html | 404 |
| Value of the Content-Type response header | text/html; charset=utf-8 |
| Remote Address (IP and port) | 127.0.0.1:5500 |
| Protocol in the address bar (http or https) | http |
 
## Why is this address http and not https?
HTTPS encrypts data transferred across a network to protect against eavesdropping.Because 127.0.0.1 represents localhost on your local machine, network traffic never leaves your computer, eliminating the need for SSL/TLS encryption during local testing.
... (two sentences)

## Specificity experiment
An ID selector (#main p) has a higher specificity weight (1,0,1) than a class and element selector combination (.hero p - 0,1,1), causing rules attached to an ID to override class-based rules regardless of their order in the CSS file.

## Selectors I used

| Selector kind | Example from my CSS |
|---|---|
| Element | `body` |
| Class | `.site-header` |
| ID | `#main` |
| Grouping (comma) | `h1, h2, h3` |
| Descendant (space) | `.nav-list a` |
| Child (>) | `main > section` |
| Adjacent sibling (+) | `h1 + p` |
| Compound (no space) | `a.active` |
| Attribute | `a[href^="http"]` |
| Pseudo-class | `a:hover` |
| Pseudo-element | `.menu-group h2::before` |


## Bug log (Lab 4, Task 6)

| # | What was wrong (file and line) | Which tool showed it | My fix |
|---|--------------------------------|----------------------|--------|
| 1 | `bugs.html`: Missing `lang` attribute on `<html>` tag | Lighthouse / W3C Validator | Added `lang="en"` to `<html>` |
| 2 | `bugs.html`: Linked stylesheet was `style.css` instead of `bugs.css` | DevTools Network Tab (404) | Fixed `<link>` href to `bugs.css` |
| 3 | `bugs.html`: Used non-semantic `div` for navigation links | DevTools Accessibility Tree | Changed `div.menu` to `<nav class="menu">` with `aria-label` |
| 4 | `bugs.html`: Heading level skipped from `h1` to `h4` | DevTools Accessibility Tree | Changed `h4` to `h2` for sequential heading order |
| 5 | `bugs.html`: `<img>` tag was missing `alt` text attribute | Lighthouse Audit | Added `alt="Campus Café logo"` to `<img>` |
| 6 | `bugs.html`: `<label for="mail">` did not match `<input id="email">` | DevTools / Manual Click Test | Updated label attribute to `for="email"` |
| 7 | `bugs.css`: Used invalid CSS property `colour` instead of `color` | DevTools Styles Pane | Fixed property spelling to `color: #ffffff;` |
| 8 | `bugs.css`: Missing semicolon after `background: #0b1f3a` in `.btn:hover` | DevTools Styles Pane | Added missing semicolon `;` after color value |
| 9 | `bugs.css`: Class selector `.notes` mismatched HTML class `note` | DevTools Elements Pane | Renamed selector to `.note`[cite: 1] |
| 10 | `bugs.css`: Muted note text `#999999` had insufficient contrast | Lighthouse Audit | Darkened color to `#595959` to pass contrast threshold[cite: 1] |