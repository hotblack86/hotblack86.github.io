# popup-dialog

Popup dialog

It is important that the popup element has the descendant
element with the attribute `role="document"`, otherwise it
will fail to open. Displayed in the center by default. Assign
`popup--full`, `popup--top`, `popup--right`, `popup--bottom` or `popup--left`
classes to the element in order to change the position of the popup.
Omit `<div class="popup__overlay"></div>` if you want the popup to
be transparent. Elements with the attribute data-a11y-dialog-show="this-modal-id"
will be set up to open this element on click. Elements with the attribute
data-a11y-dialog-hide inside the popup will be set up to close
the popup on click.

## Example

```html
<caption>Basic usage</caption>
<popup-dialog
id="unique-popup-id"
class="
popup
popup--full
"
data-disable-body-scroll
data-open-on-page-load="1000"
data-remember-state="14"
aria-hidden="true"
aria-labelledby="unique-popup-title"
role="ariadialog"
>
<div class="popup__overlay"></div>
<div class="popup__wrapper">
<div class="popup__content" role="document">
<h3 id="unique-popup-title">Popup title</h3>
<button
title="{{ 'layout.drawers.close' | t }}"
type="button"
class="popup__close"
aria-label="{{ 'layout.drawers.close' | t }}"
data-a11y-dialog-hide
>
<i class="icon icon--close-l"></i>
</button>
...
</div>
</div>
</popup-dialog>
```

## Attributes

| Attribute                     | Description                                      |
|-------------------------------|--------------------------------------------------|
| `data-disable-body-scroll`    | Disable body scrolling                           |
| `data-dismiss-after-interval` | Dismiss the dialog after<br />the specified interval in milliseconds |
| `data-open-on-page-load`      | Open the dialog on page<br />load. Optional delay can be provided in milliseconds |
| `data-remember-state`         | Remember the dialog state<br />on popup close. Optional cookie expiry date in days<br />can be provided, otherwise session cookie is created |
| `role`                        | Popup role. Id set to "alertdialog", hitting<br />"Escape" key will not dismiss it |

## Properties

| Property | Modifiers | Type      | Description             |
|----------|-----------|-----------|-------------------------|
| `shown`  | readonly  | `boolean` | Get popup dialog status |

## Methods

| Method           | Type                                             | Description                                      |
|------------------|--------------------------------------------------|--------------------------------------------------|
| `#onClosing`     | `(): void`                                       |                                                  |
| `#onHide`        | `(): void`                                       |                                                  |
| `#onMouseEnter`  | `(): void`                                       |                                                  |
| `#onMouseLeave`  | `(): void`                                       |                                                  |
| `#onOpening`     | `(): void`                                       |                                                  |
| `#onShow`        | `(): void`                                       |                                                  |
| `close`          | `(): Promise`                                    | Close popup                                      |
| `closeInstantly` | `(): void`                                       | Close popup instantly<br /><br />Closes popup instantly even if animations are set<br />to content element |
| `off`            | `(type: any, handler: any, options: any): PopupDialog` | Remove event listener                            |
| `on`             | `(type: any, handler: any, options: any): PopupDialog` | Add event listener                               |
| `open`           | `(): Promise`                                    | Open modal                                       |
| `openInstantly`  | `(): void`                                       | Open popup instantly<br /><br />Opens popup instantly even if animations are set<br />to content element |

## Events

| Event              | Type               | Description            |
|--------------------|--------------------|------------------------|
| `on:popup:closed`  | `CustomEvent<any>` | Popup finished closing |
| `on:popup:closing` | `CustomEvent<any>` | Popup started closing  |
| `on:popup:opened`  | `CustomEvent<any>` | Popup finished opening |
| `on:popup:opening` | `CustomEvent<any>` | Popup started opening  |

## CSS Custom Properties

| Property                   | Description            |
|----------------------------|------------------------|
| `--background-color`       | Popup background color |
| `--close-button-font-size` | Close button icon size |
| `--close-button-size`      | Close button size      |
| `--closing-speed`          | Popup closing speed    |
| `--color`                  | Popup text color       |
| `--opening-speed`          | Popup opening speed    |
| `--width`                  | Popup max width        |
