# modal-dialog

Modal component

It is important that the modal element has the descendant
element with the attribute `role="document"`, otherwise it
will fail to open. Displayed on the left by default. Assign
`modal--right` or `modal--top` classes to the element in
order to change the position of the modal. Elements with the
attribute `data-a11y-dialog-show="this-modal-id"` will be set
up to open this element on click. Elements with the attribute
`data-a11y-dialog-hide` inside the modal will be set up to close
the modal on click.

## Example

```html
<caption>Basic usage</caption>
<modal-dialog
id="unique-modal-id"
class="modal modal--right"
aria-labelledby="unique-modal-id-title"
aria-hidden="true"
>
<div class="modal__overlay" data-a11y-dialog-hide></div>
<div class="modal__wrapper" role="document">
<div class="modal__content">
<h3 id="unique-modal-id-title">Modal title</h3>
<button
title="{{ 'layout.drawers.close' | t }}"
type="button"
class="modal__close"
aria-label="{{ 'layout.drawers.close' | t }}"
data-a11y-dialog-hide
>
<i class="icon icon--close-l"></i>
</button>
...
</div>
</div>
</modal-dialog>
```

## Properties

| Property | Modifiers | Type      | Description             |
|----------|-----------|-----------|-------------------------|
| `shown`  | readonly  | `boolean` | Get modal dialog status |

## Methods

| Method           | Type                                             | Description                                      |
|------------------|--------------------------------------------------|--------------------------------------------------|
| `#onClosing`     | `(): void`                                       |                                                  |
| `#onHide`        | `(): void`                                       |                                                  |
| `#onOpening`     | `(): void`                                       |                                                  |
| `#onShow`        | `(): void`                                       |                                                  |
| `close`          | `(): Promise`                                    | Close modal                                      |
| `closeInstantly` | `(): void`                                       | Close modal instantly<br /><br />Closes modal instantly even if animations are set<br />to content element |
| `destroy`        | `(): void`                                       | Destroy modal<br /><br />Remove modal attributes abd listeners |
| `init`           | `(): void`                                       | Initialize modal<br /><br />Set up the dialog instance, assign the content element,<br />set up triggers and listeners |
| `off`            | `(type: any, handler: any, options: any): ModalDialog` | Remove event listener                            |
| `on`             | `(type: any, handler: any, options: any): ModalDialog` | Add event listener                               |
| `open`           | `(openElementAfterClose?: HTMLElement): Promise` | Open modal<br /><br />**openElementAfterClose**: Modal to open after this modal is closed |
| `openInstantly`  | `(): void`                                       | Open modal instantly<br /><br />Opens modal instantly even if animations are set<br />to content element |

## Events

| Event              | Type               | Description            |
|--------------------|--------------------|------------------------|
| `on:modal:closed`  | `CustomEvent<any>` | Modal finished closing |
| `on:modal:closing` | `CustomEvent<any>` | Modal started closing  |
| `on:modal:opened`  | `CustomEvent<any>` | Modal finished opening |
| `on:modal:opening` | `CustomEvent<any>` | Modal started opening  |

## CSS Custom Properties

| Property                   | Description                           |
|----------------------------|---------------------------------------|
| `--background-color`       | Modal background color                |
| `--close-button-font-size` | Close button icon size                |
| `--close-button-size`      | Close button size                     |
| `--closing-speed`          | Modal closing speed                   |
| `--color`                  | Modal text color                      |
| `--opening-speed`          | Modal opening speed                   |
| `--width`                  | Modal width (if placed right or left) |
