# video-player

Video player

## Example

```html
<caption>Basic usage</caption>
<video-player
data-type="youtube"
data-poster="{{ media.preview_image | image_url: width: 1946 }}"
style="--aspect-ratio: {{ media.preview_image.width }} / {{ media.preview_image.height }}""
>
<video-poster>
{{ media.preview_image | image_url: width: 1946 | image_tag:
loading: lazy,
sizes: sizes,
widths: '246, 493, 600, 713, 823, 990, 1100, 1206, 1346, 1426, 1646, 1946'
}}
</video-poster>
{% render 'theme-spinner', tag: 'video-loading-indicator', hidden: true %}
<video-element></video-element>
<template>
<div id="{{ section.id | append: '--' | append: media.id }}" video-element data-{{- media.host -}}-id="{{ media.external_id }}"></div>
<!-- for native video
<video video-element src="media.sources[0].url"></video>
-->
</template>
</video-player>
```

## Attributes

| Attribute     | Description                                      |
|---------------|--------------------------------------------------|
| `data-poster` | Poster (Optional: useful for external videos to replace the default one) |
| `data-type`   | Video type ("html5", "youtube", "vimeo")         |

## Properties

| Property | Modifiers | Type      | Description             |
|----------|-----------|-----------|-------------------------|
| `ready`  | readonly  | `boolean` | Get video player status |

## Methods

| Method        | Type                                             | Description                                      |
|---------------|--------------------------------------------------|--------------------------------------------------|
| `loadContent` | `(): VideoPlayer`                                | Load video content                               |
| `off`         | `(type: string, handler: Function, options?: string): VideoPlayer` | Remove event listener<br /><br />**type**: Event type<br />**handler**: Event handler<br />**options**: Event options |
| `on`          | `(type: string, handler: Function, options?: string): VideoPlayer` | Add event listener<br /><br />**type**: Event type<br />**handler**: Event handler<br />**options**: Event options |
| `pause`       | `(): VideoPlayer`                                | Pause video                                      |
| `play`        | `(): VideoPlayer`                                | Play video                                       |

## Events

| Event                   | Type               | Description                |
|-------------------------|--------------------|----------------------------|
| `on:video-player:ready` | `CustomEvent<any>` | Fired when player is ready |
