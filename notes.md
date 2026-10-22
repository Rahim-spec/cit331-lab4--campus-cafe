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