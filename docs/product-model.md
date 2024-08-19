# product-model

A custom element that extends DeferredMedia to load and set up 3D model viewers
for product pages. It integrates Shopify's Model Viewer UI for enhanced interaction
with 3D models.

## Example

```html
<caption>Basic usage</caption>
<product-model
class="
media-gallery__item
media-gallery__item--model
deferred-media
"
data-slide-id="{{ forloop.index0 }}"
data-media-id="{{ media.id }}"
>
<media-poster>
{{ media.preview_image | image_url: width: 1946 | image_tag:
loading: lazy,
sizes: sizes,
widths: '246, 493, 600, 713, 823, 990, 1100, 1206, 1346, 1426, 1646, 1946'
}}
</media-poster>
<template>
{{ media | media_tag: image_size: "2048x", toggleable: true }}
</template>
</product-model>
```

## Methods

| Method               | Type                    | Description                                      |
|----------------------|-------------------------|--------------------------------------------------|
| `loadContent`        | `(): void`              | Loads the necessary content and initializes the Shopify Model Viewer UI.<br />Overrides the `loadContent` method from DeferredMedia. |
| `setupModelViewerUI` | `(errors: Array): void` | Sets up the Shopify Model Viewer UI by attaching it to the `model-viewer` element.<br />Dispatches a custom event when the model is loaded.<br /><br />**errors**: An array of errors that may occur during setup. |

## Events

| Event                     | Type               | Description                     |
|---------------------------|--------------------|---------------------------------|
| `on:product-model:loaded` | `CustomEvent<any>` | Fired when the model is loaded. |
