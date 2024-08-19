# image-skeleton

Image Skeleton
A custom web component that provides a skeleton loader for images to enhance loading performance.
This component displays a placeholder while an image is loading, and only reveals the image once it has fully loaded.

## Example

```html
<caption>Basic usage</caption>
<image-skeleton minimum-reveal-delay="250">
<span class="visually-hidden">Image alt text</span>
<svg
id="visual"
viewBox="0 0 400 300"
width="400"
height="300"
xmlns="http://www.w3.org/2000/svg"
>
<rect x="0" y="0" width="400" height="300"></rect>
</svg>
</image-skeleton>
```

## Attributes

| Attribute              | Type      | Description                                     |
|------------------------|-----------|-------------------------------------------------|
| `loaded`               | `boolean` | If true, the image has already been loaded.     |
| `minimum-reveal-delay` | `number`  | The minimum delay before the image is revealed. |

## Methods

| Method         | Type       | Description                                      |
|----------------|------------|--------------------------------------------------|
| `init`         | `(): void` | Initializes the skeleton loader by checking the associated image element.<br />Sets up an event listener to reveal the image after it has fully loaded. |
| `markAsLoaded` | `(): void` | Marks the skeleton loader as loaded and hides it.<br />Sets the 'loaded' and 'aria-hidden' attributes. |
