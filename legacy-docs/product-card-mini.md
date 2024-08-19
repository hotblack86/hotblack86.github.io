# product-card-mini

## Properties

| Property  | Type             |
|-----------|------------------|
| `id`      | `string \| null` |
| `product` |                  |

## Methods

| Method                     | Type                                             |
|----------------------------|--------------------------------------------------|
| `#onQuickShopTriggerClick` | `(event: any): Promise<void>`                    |
| `renderImage`              | `(url: any, width: any, height: any, classes?: string, alt?: string, sizes?: string, srcsetWidths?: number[]): HTMLImageElement \| null` |
| `updateImage`              | `(url: any, width: any, height: any, alt?: string, srcsetWidths?: number[]): void` |
| `updateSkeleton`           | `(): void`                                       |


# product-card

## Properties

| Property  | Type             |
|-----------|------------------|
| `id`      | `string \| null` |
| `product` |                  |

## Methods

| Method                     | Type                                             |
|----------------------------|--------------------------------------------------|
| `#onQuickShopTriggerClick` | `(event: any): Promise<void>`                    |
| `#removeSwatchesListeners` | `(): void`                                       |
| `#setProductData`          | `(): void`                                       |
| `#setUpSwatchesListeners`  | `(): void`                                       |
| `renderImage`              | `(url: any, width: any, height: any, classes?: string, alt?: string, sizes?: string, srcsetWidths?: number[]): HTMLImageElement \| null` |
| `setVariant`               | `(e: any): void`                                 |
| `updateImage`              | `(url: any, width: any, height: any, alt?: string, srcsetWidths?: number[]): void` |
| `updateSkeleton`           | `(): void`                                       |
