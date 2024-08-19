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
{% render 'icons-theme', icon: 'close' %}
</button>
<div
class="popup__content"
role="document"
>
{% render 'video-player',
id: video_player_id,
video_type: 'html5',
video: video_file,
poster_image_sizes: '(min-width: 990px) 990px, calc(100vw - 36px)'
%}
</div>
</div>
</video-dialog>
```

## Methods

| Method              | Type       |
|---------------------|------------|
| `#loadVideoAndPlay` | `(): void` |
| `#pauseVideo`       | `(): void` |
