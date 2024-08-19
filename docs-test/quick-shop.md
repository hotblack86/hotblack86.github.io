# quick-shop

## Properties

| Property    |
|-------------|
| `variantId` |

## Methods

| Method                       | Type                                             |
|------------------------------|--------------------------------------------------|
| `#fetchQuickShop`            | `(): Promise<void>`                              |
| `#fetchQuickShopOnProximity` | `(entries: any, observer: any): Promise<void>`   |
| `#onCloseModal`              | `(): void`                                       |
| `#onOpenModal`               | `(): void`                                       |
| `#onVariantChange`           | `(event: any): void`                             |
| `#removeFetchListeners`      | `(): void`                                       |
| `#setProductData`            | `(): void`                                       |
| `#setUpFetchListeners`       | `(): void`                                       |
| `#updateContent`             | `(newContent: any): void`                        |
| `#updateImage`               | `(url: any, width: any, height: any, alt?: string, srcsetWidths?: number[]): void` |
| `#updateVariant`             | `(): void`                                       |
| `close`                      | `(): Promise<any>`                               |

## Events

| Event                   | Type               |
|-------------------------|--------------------|
| `on:quick-shop:failed`  | `CustomEvent<any>` |
| `on:quick-shop:loaded`  | `CustomEvent<any>` |
| `on:quick-shop:loading` | `CustomEvent<any>` |
