# Chapter landmarks

ocCitizen can include chapter titles in the table of contents without making
them collapsible article headings. Give the rendered element a unique `id` and
the `citizen-toc-landmark` class.

```html
<div id="chapter-01" class="citizen-toc-landmark">Chapter 01: The vineyard</div>
```

When using a Lua module, add the class and ID to the chapter title element
through `mw.html`. The title then appears alongside normal headings in page
order and participates in the current-section display on mobile.

Optional attributes:

| Attribute | Behavior |
| --- | --- |
| `data-citizen-toc-label` | Overrides the label; otherwise the element's text is used. |
| `data-citizen-toc-level` | Sets a nesting level from 1 to 6; defaults to 1. |
| `data-citizen-toc-number` | Supplies a section number when numbers are displayed. |

Labels are treated as plain text. Each ID should be unique across both
landmarks and ordinary headings. Pages with only landmarks also receive a
table of contents. Landmark entries require JavaScript.

On mobile, the page tools strip is hidden when it contains no unselected
actions, allowing a toolbar containing only the More button to remain square.
