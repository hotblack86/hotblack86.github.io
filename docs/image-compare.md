# image-compare

Custom element for comparing images with a sliding effect.
Allows users to adjust the exposure level of an image via a slider.
Also includes an intersection observer to animate the slider when it enters the viewport.

## Example

```html
<caption>Basic usage</caption>
<image-compare
style="
--exposure: 50%;
--thumb-border-color: #ff0000;
--divider-color: #ff0000;
--thumb-background-color: #ffffff;
--image-background-color: #000000;
"
data-start-point="50"
data-grow-thumb="true"
>

<div class="image-compare__media-item image-compare__media-item--before">
<div class="o-ratio o-ratio--16by9 o-ratio--16by9@mob">
<div class="o-ratio__content">
<img src="image1.jpg" alt="Before Image" class="image-compare__image" />
<div class="image-compare__image-background"></div>
</div>
</div>
</div>

<div class="image-compare__media-item image-compare__media-item--after">
<div class="o-ratio o-ratio--16by9 o-ratio--16by9@mob">
<div class="o-ratio__content">
<img src="image2.jpg" alt="After Image" class="image-compare__image" />
<div class="image-compare__image-background"></div>
</div>
</div>
</div>

<label>
<span class="u-hidden-visually">Control how much of each overlapping image is shown</span>
<input type="range" value="50" min="0" max="100" step="0.1">
</label>
</image-compare>
```

## Attributes

| Attribute          | Type      | Description                                 |
|--------------------|-----------|---------------------------------------------|
| `data-grow-thumb`  | `boolean` | If true, the thumb will grow when hovered.  |
| `data-start-point` | `string`  | The initial exposure value as a percentage. |

## CSS Custom Properties

| Property                   | Description                              |
|----------------------------|------------------------------------------|
| `--divider-color`          | The color of the divider line.           |
| `--exposure`               | The current exposure level of the image. |
| `--image-background-color` | The background color of the images.      |
| `--thumb-background-color` | The background color of the thumb.       |
| `--thumb-border-color`     | The border color of the thumb.           |
