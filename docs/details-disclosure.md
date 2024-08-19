# details-disclosure

A custom element that manages the disclosure of content within a `details` element.
It handles focus out and toggle events to control animations and visibility.

## Properties

| Property            | Type         | Default              |
|---------------------|--------------|----------------------|
| `content`           | `any \| any` | "nextElementSibling" |
| `mainDetailsToggle` | `any \| any` |                      |

## Methods

| Method       | Type       | Description                                      |
|--------------|------------|--------------------------------------------------|
| `close`      | `(): void` | Closes the disclosure by removing the `open` attribute from the `details` element<br />and setting `aria-expanded` to false on the `summary` element. |
| `onFocusOut` | `(): void` | Handles the focusout event on the `details` element.<br />Closes the disclosure if the focus moves outside the element. |
| `onToggle`   | `(): void` | Handles the toggle event on the `details` element.<br />Plays or cancels animations based on whether the `details` element is open. |
