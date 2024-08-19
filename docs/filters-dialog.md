# filters-dialog

A custom element that extends `ModalDialog` to provide a modal dialog with filters.
It initializes and destroys the dialog based on the viewport width and media query changes.

## Attributes

| Attribute                       | Type      | Description                |
|---------------------------------|-----------|----------------------------|
| `data-disable-modal-on-desktop` | `boolean` | Disables modal on desktop. |

## Methods

| Method    | Type       | Description                                      |
|-----------|------------|--------------------------------------------------|
| `destroy` | `(): void` | Destroys the dialog by removing ARIA attributes and CSS classes.<br />Calls the parent class's `destroy` method. |
| `init`    | `(): void` | Initializes the dialog by setting ARIA attributes and CSS classes.<br />Calls the parent class's `init` method. |
