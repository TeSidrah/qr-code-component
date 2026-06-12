# QR Code Component

A responsive QR code component built with HTML and CSS.

## What it demonstrates

The card is a single `div` inside `<main>`. `<section>` was considered and 
rejected — the page has one part, not several, and `<section>` would 
misrepresent that.

Colors and font weights are set as CSS custom properties on `:root`, 
scoped to the values that actually vary between elements rather than 
wrapping everything in a variable.

The card's width is `90%` with `max-width: 320px`, so it scales down on 
small screens and caps out on larger ones. The QR image is `width: 100%`, 
so it always tracks the card's width.

Padding uses `rem` rather than `%` — `%` padding is calculated from the 
parent's width even for top/bottom spacing, which would make vertical 
spacing shift with screen width for no reason.

`<main>` is set to `display: contents`. Found by adding a debug outline to 
every element and seeing that `<main>`'s default box was adding extra 
space on one side of the card. `display: contents` removes that box from 
the layout — so the card becomes a direct flex child of `<body>` and 
centers correctly — while keeping `<main>` in the document for 
accessibility and structure.

Google Fonts is loaded with `preconnect` hints, so the browser opens the 
connection to the font server while the rest of the document is still 
being parsed.

## Live preview

[Add once GitHub Pages is enabled]

## Challenge

Frontend Mentor — QR code component
[Add link to challenge page]
