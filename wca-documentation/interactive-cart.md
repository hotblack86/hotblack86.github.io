# interactive-cart

## Methods

| Method                 | Type                   |
|------------------------|------------------------|
| `#onResize`            | `(entries: any): void` |
| `#render`              | `(): void`             |
| `#renderCart`          | `(): void`             |
| `#renderEmptyCart`     | `(): void`             |
| `#updateCartDiscounts` | `(): void`             |
| `#updateCartTotal`     | `(): void`             |
| `#updateFreeShipping`  | `(): void`             |


# cart-items


# cart-item

## Methods

| Method                          | Type                              |
|---------------------------------|-----------------------------------|
| `#changeQuantity`               | `(): Promise<void>`               |
| `#clearTotalPrice`              | `(): void`                        |
| `#removeProduct`                | `(e: any): Promise<void>`         |
| `#render`                       | `(): void`                        |
| `#renderError`                  | `(errorText?: string): void`      |
| `#renderTotalPriceAndDiscounts` | `(): void`                        |
| `#setImage`                     | `(srcsetWidths?: number[]): void` |
| `#toggleSpinner`                | `(visible?: boolean): void`       |
| `#updateSkeleton`               | `(): void`                        |


# discount-list

## Properties

| Property | Attribute |
|----------|-----------|
| `items`  | `items`   |

## Methods

| Method             | Type       |
|--------------------|------------|
| `#renderDiscounts` | `(): void` |


# cart-textarea

## Properties

| Property      |
|---------------|
| `function`    |
| `updated`     |
| `updatedHTML` |
| `updating`    |
| `value`       |


# cart-gift-wrapping-message


# cart-note


# cart-spinner


# cart-terms

## Methods

| Method          | Type                                             |
|-----------------|--------------------------------------------------|
| `#inputChange`  | `({ target: { checked } }: { target: { checked: any; }; }): void` |
| `#toggleError`  | `(visible?: boolean): void`                      |
| `#validateForm` | `(e: any): void`                                 |


# cart-notification

## Methods

| Method            | Type                              |
|-------------------|-----------------------------------|
| `#render`         | `(): void`                        |
| `#setImage`       | `(srcsetWidths?: number[]): void` |
| `#updateSkeleton` | `(): void`                        |


# cart-quantity-info

## Properties

| Property      | Type         |
|---------------|--------------|
| `infoContent` | `any \| any` |
| `itemsCount`  | `any \| any` |


# cart-gift-wrapping-banner

## Methods

| Method        | Type                                             |
|---------------|--------------------------------------------------|
| `#enable`     | `(e: any): Promise<void>`                        |
| `#setIsDoing` | `(isDoing?: boolean, error?: boolean): Promise<any>` |
