# quick-shop

A custom HTML element that represents a Quick Shop modal dialog, extending the ModalDialog class.

This element handles displaying a quick shop modal with product details, including variant updates and media handling.
It also manages modal opening/closing events and fetches quick shop content based on proximity or user interaction.

## Example

```html
<caption>Basic usage</caption>
<quick-shop
data-product-url="https://example.com/product-url"
image-container-ratio="16:9"
image-sizes="(min-width: 600px) 50vw, 100vw"
image-fit
load-on="click"
placeholder
card-id="product-card-123"
aria-labelledby="quick-shop-title"
aria-hidden="true"
>
<!-- Modal content goes here -->
</quick-shop>
```

## Attributes

| Attribute               | Type      | Description                                      |
|-------------------------|-----------|--------------------------------------------------|
| `aria-hidden`           | `boolean` | Indicates whether the component is hidden from accessibility tools. |
| `aria-labelledby`       | `string`  | The ID of the element used to label the component for accessibility. |
| `card-id`               | `string`  | The ID associated with the product card.         |
| `data-product-url`      | `string`  | The URL of the product to display.               |
| `image-container-ratio` | `string`  | The aspect ratio of the image container.         |
| `image-fit`             | `boolean` | Whether to fit the image to the container.       |
| `image-sizes`           | `string`  | The sizes attribute for responsive images.       |
| `notify-on-add`         | `boolean` | Whether to notify on adding the product to the cart. |
| `placeholder`           | `boolean` | Whether to display a placeholder image if no product image is available. |

## Properties

| Property    | Type               | Description                                      |
|-------------|--------------------|--------------------------------------------------|
| `variantId` | `string \| number` | Sets the current variant ID and updates the variant. |

## Methods

| Method  | Type         | Description                                      |
|---------|--------------|--------------------------------------------------|
| `close` | `(): string` | Closes the quick shop modal and resolves with a 'Closed' message. |

## Events

| Event                   | Type               | Description                                      |
|-------------------------|--------------------|--------------------------------------------------|
| `on:quick-shop:failed`  | `CustomEvent<any>` | Fired when the quick shop content fails to load. |
| `on:quick-shop:loaded`  | `CustomEvent<any>` | Fired when the quick shop content has been successfully loaded. |
| `on:quick-shop:loading` | `CustomEvent<any>` | Fired when the quick shop content starts loading. |
