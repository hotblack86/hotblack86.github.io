# product-card-swatches

Custom HTML element representing a product card with swatches.
This element allows users to select different product variants by clicking on swatches,
which updates the product image and variant link.

## Properties

| Property      | Type                  |
|---------------|-----------------------|
| `hoverImage`  | `any \| any`          |
| `image`       | `any \| any`          |
| `product`     | `any \| any`          |
| `productLink` | `any \| any`          |
| `triggers`    | `NodeListOf<Element>` |

## Methods

| Method                   | Type                             | Description                                      |
|--------------------------|----------------------------------|--------------------------------------------------|
| `updateCardImage`        | `(swatch: HTMLElement): boolean` | Updates the product card image and product variant link based on the selected swatch.<br /><br />**swatch**: The swatch element that was clicked. |
| `updateQuickShopVariant` | `(swatch: HTMLElement): void`    | Updates the quick shop variant with the selected swatch's variant ID.<br /><br />**swatch**: The swatch element that was clicked. |
