# product-card-mini

A custom element that represents a mini product card.
Handles rendering of product details, image updates, and quick shop functionality.

## Example

```html
<caption>Basic usage</caption>
<product-card-mini
rendered
data-product-id="{{ current_product.id }}"
class="{{ product_card_classes }}"
image-container-ratio="{{ container_ratio }}"
image-fit
section-id="{{ section_id }}"
quick-shop-trigger="{{ quick_shop_trigger }}"
move-quick-shop
>
<a product-card-link href="{{ link }}" class="product-card__link">
<span class="visually-hidden">{{ title }}</span>
</a>
<div class="product-card__top">
<div class="o-ratio o-ratio--{{ container_ratio }}"
style="padding-bottom:{{ image_container_bottom_padding }}">
<div class="o-ratio__content">
<a product-card-link href="{{ link }}" tabindex="-1">
 <div class="product-card__media product-card__media--hover-image">
   <product-card-secondary-image-placeholder
     class="product-card__img-hover hover-enabled">
     {% render 'image', image: secondary_image, additional_classes: 'product-card__img-hover hover-enabled' %}
   </product-card-secondary-image-placeholder>
   {% render 'image', image: image, additional_classes: 'product-card__img js-product-card-image' %}
 </div>
</a>
</div>
</div>
</div>
<div class="product-card__details">
<h3 class="product-card__title">
<product-card-title>{{ current_product.title }}</product-card-title>
</h3>
<product-card-price class="product-card__price">
{% render 'product-price', product: current_product %}
</product-card-price>
<product-card-button class="product-card-btn">
<button type="button" class="link" disabled="disabled">{{ 'products.product.sold_out' | t }}</button>
</product-card-button>
</div>
</product-card-mini>
```

## Attributes

| Attribute               | Type      | Description                                      |
|-------------------------|-----------|--------------------------------------------------|
| `image-container-ratio` | `string`  | The ratio of the image container (e.g., "natural"). |
| `image-fit`             | `boolean` | Determines if the image should fit within its container. |
| `image-hover`           | `boolean` | Determines the hover effect for the image (e.g., "zoom"). |
| `move-quick-shop`       | `boolean` | Indicates if the quick shop should be moved to a different container. |
| `quick-shop-trigger`    | `string`  | Specifies the type of quick shop trigger (e.g., "button"). |
| `rendered`              | `boolean` | Indicates if the product card has been rendered. |

## Properties

| Property  | Attribute | Type     | Description                                      |
|-----------|-----------|----------|--------------------------------------------------|
| `id`      | `id`      | `string` | Sets the ID of the product card and updates the quick shop ID if present. |
| `product` |           |          | Sets the product data and triggers the rendering process if necessary. |

## Methods

| Method           | Type                                             | Description                                      |
|------------------|--------------------------------------------------|--------------------------------------------------|
| `renderImage`    | `(url: string, width: number, height: number, classes?: string \| undefined, alt?: string \| undefined, sizes?: string \| undefined, srcsetWidths?: number[] \| undefined): HTMLImageElement\|null` | Renders an image element with the provided URL, width, and height,<br />and optional classes, alt text, and sizes. The image is created with<br />a srcset attribute for responsive images.<br /><br />**url**: The URL of the image.<br />**width**: The width of the image.<br />**height**: The height of the image.<br />**classes**: The classes to apply to the image element.<br />**alt**: The alt text for the image.<br />**sizes**: The sizes attribute for the image.<br />**srcsetWidths**: The widths for the srcset attribute. |
| `updateImage`    | `(url: string, width: number, height: number, alt?: string \| undefined, srcsetWidths?: number[] \| undefined): void` | Updates the image element with the provided URL, width, height, and alt text.<br />It also generates a srcset attribute for responsive images based on the provided srcsetWidths.<br /><br />**url**: The URL of the image.<br />**width**: The width of the image.<br />**height**: The height of the image.<br />**alt**: The alt text of the image.<br />**srcsetWidths**: An array of widths for the srcset. |
| `updateSkeleton` | `(): void`                                       | Updates the skeleton element associated with the image.<br />It checks if the image has a sibling element with the tag name 'image-skeleton' and updates its attributes accordingly. |


# product-card

Custom HTML element representing a product card.
This element extends the ProductCardMini class and provides additional functionality specific to the product card.

## Example

```html
<caption>Basic usage</caption>
<product-card
rendered
data-product-id="12345"
class="product-card--custom"
image-container-ratio="1:1"
image-hover="zoom"
image-fit
section-id="featured-products"
quick-shop-trigger="icon"
move-quick-shop
>
<div class="product-card-top">
<a product-card-link href="/product/12345" class="product-card__link">
<div class="product-card__media product-card__media--hover-zoom">
<img src="/path/to/image.jpg" alt="Product Image" class="product-card__img" />
</div>
</a>
</div>
<div class="product-card__details">
<a product-card-link href="/product/12345" class="product-card__link">
<h3 class="product-card__title">Product Title</h3>
</a>
<div class="product-card__details__hover">
<product-card-price class="price">$29.99</product-card-price>
<product-card-reviews class="review-wrapper">
<div class="rating" role="img" aria-label="Rated 4.5 out of 5 stars">
 <span class="rating-star" style="--rating: 4.5;"></span>
</div>
<p class="rating-count">(150 reviews)</p>
</product-card-reviews>
</div>
</div>
</product-card>
```

## Attributes

| Attribute               | Type      | Description                                      |
|-------------------------|-----------|--------------------------------------------------|
| `image-container-ratio` | `string`  | The ratio of the image container (e.g., "natural"). |
| `image-fit`             | `boolean` | Determines if the image should fit within its container. |
| `image-hover`           | `boolean` | Determines the hover effect for the image (e.g., "zoom"). |
| `move-quick-shop`       | `boolean` | Indicates if the quick shop should be moved to a different container. |
| `quick-shop-trigger`    | `string`  | Specifies the type of quick shop trigger (e.g., "button"). |
| `rendered`              | `boolean` | Indicates if the product card has been rendered. |

## Properties

| Property  | Attribute | Type     | Description                                      |
|-----------|-----------|----------|--------------------------------------------------|
| `id`      | `id`      | `string` | Sets the ID of the product card and updates the quick shop ID if present. |
| `product` |           |          | Sets the product data and updates the current variant URL and swatches listeners if necessary. |

## Methods

| Method           | Type                                             | Description                                      |
|------------------|--------------------------------------------------|--------------------------------------------------|
| `renderImage`    | `(url: string, width: number, height: number, classes?: string \| undefined, alt?: string \| undefined, sizes?: string \| undefined, srcsetWidths?: number[] \| undefined): HTMLImageElement\|null` | Renders an image element with the provided URL, width, and height,<br />and optional classes, alt text, and sizes. The image is created with<br />a srcset attribute for responsive images.<br /><br />**url**: The URL of the image.<br />**width**: The width of the image.<br />**height**: The height of the image.<br />**classes**: The classes to apply to the image element.<br />**alt**: The alt text for the image.<br />**sizes**: The sizes attribute for the image.<br />**srcsetWidths**: The widths for the srcset attribute. |
| `setVariant`     | `(e: Event): void`                               | Updates the product variant based on the selected variant ID.<br /><br />**e**: The event object triggered by the variant selection. |
| `updateImage`    | `(url: string, width: number, height: number, alt?: string \| undefined, srcsetWidths?: number[] \| undefined): void` | Updates the image element with the provided URL, width, height, and alt text.<br />It also generates a srcset attribute for responsive images based on the provided srcsetWidths.<br /><br />**url**: The URL of the image.<br />**width**: The width of the image.<br />**height**: The height of the image.<br />**alt**: The alt text of the image.<br />**srcsetWidths**: An array of widths for the srcset. |
| `updateSkeleton` | `(): void`                                       | Updates the skeleton element associated with the image.<br />It checks if the image has a sibling element with the tag name 'image-skeleton' and updates its attributes accordingly. |
