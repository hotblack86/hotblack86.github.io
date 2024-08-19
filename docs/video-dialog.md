# video-dialog

Video popup dialog

Load and plays the video when opened, pauses on close
Inherits all the methods and events of PopupDialog class

## Example

```html
<caption>Basic usage</caption>
<video-dialog
id="video-dialog-unique-id"
class="
popup
popup--video
"
data-disable-body-scroll
aria-hidden="true"
>
<div class="popup__overlay" data-a11y-dialog-hide></div>

<div class="popup__wrapper">
<button
title="{{ 'layout.drawers.close' | t }}"
type="button"
class="popup__close"
aria-label="{{ 'layout.drawers.close' | t }}"
data-a11y-dialog-hide
>
<i class="icon icon--close-l"></i>
</button>
<div
class="popup__content"
role="document"
>
<video>
</video>
</div>
</div>
</video-dialog>
```

## Methods

| Method              | Type       |
|---------------------|------------|
| `#loadVideoAndPlay` | `(): void` |
| `#pauseVideo`       | `(): void` |
