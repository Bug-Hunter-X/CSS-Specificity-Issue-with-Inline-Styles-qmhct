# CSS Specificity Issue with Inline Styles

This repository demonstrates an uncommon bug related to CSS specificity where inline styles unexpectedly override styles set by more specific selectors.  The bug arises when inline styles are applied to elements, potentially overriding styles defined with higher specificity in the CSS.

## Bug Description

The core problem lies in how CSS handles inline styles and the cascading nature of stylesheets.  Inline styles (styles directly within an HTML element) generally take precedence over styles defined in external or internal stylesheets, regardless of specificity.

## How to Reproduce

1. Clone this repository.
2. Open `bug.html` in a web browser.
3. Observe that the paragraph with class `special` has a font size of 16px, even though `p.special` is more specific than `.container p`.  This is due to the higher precedence of the inline style.

## Solution

The solution involves using a more specific selector (like an ID selector), or removing/avoiding inline styles for better control and predictability in CSS specificity.  Review the `bugSolution.css` file for a demonstration.