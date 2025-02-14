# CSS :hover and Sibling Selectors (+): Unexpected Behavior

This repository demonstrates an uncommon bug related to the unexpected behavior of the CSS `:hover` pseudo-class when used in conjunction with the `+` (adjacent sibling) selector. The bug occurs when attempting to style a sibling element based on the hover state of a preceding element.  The effect doesn't propagate as expected beyond the immediate next sibling.

## Bug Description

The provided CSS uses the `:hover` pseudo-class and the `+` sibling selector to change the background color of a sibling element upon hovering over another.  The issue is that this only works reliably when the hovered element is the first element. Hovering on subsequent elements will not apply the style to the following element as anticipated.

## Solution

The solution requires a more robust approach using the `:hover ~` (general sibling selector), or perhaps even Javascript for more complex scenarios.

## How to Reproduce

1. Clone the repository.
2. Open `bug.html` in a web browser.
3. Observe the unexpected behavior when hovering on different boxes.