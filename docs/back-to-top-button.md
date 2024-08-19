# back-to-top-button

Custom element that displays a "Back to Top" button.
The button appears when the user scrolls past the viewport height and scrolls the page back to the top when clicked.

## Example

```html
<caption>Basic usage</caption>
<back-to-top-button
class="back-to-top-button back-to-top-button--blue back-to-top-button--square"
aria-label="Back to top"
type="button"
role="button"
tabindex="0"
align-right
>
{% render 'icons-theme', icon: 'chevron', additional_classes: 'back-to-top-button__icon icon--up' %}
<span class="visually-hidden">Back to top</span>
</back-to-top-button>
```

## Properties

| Property           |
|--------------------|
| `scrollToTop`      |
| `toggleVisibility` |

## Methods

| Method             | Type       | Description                                      |
|--------------------|------------|--------------------------------------------------|
| `scrollToTop`      | `(): void` | Scrolls to the top of the page smoothly or instantly. Dispatches a custom event when the button is clicked. |
| `toggleVisibility` | `(): void` | Toggles the visibility of the button based on scroll position. The button is visible when the user has scrolled past the viewport height. |

## Events

| Event                           | Type               | Description                       |
|---------------------------------|--------------------|-----------------------------------|
| `on:back-to-top-button:clicked` | `CustomEvent<any>` | Fired when the button is clicked. |
