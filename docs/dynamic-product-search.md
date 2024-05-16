# dynamic-product-search

## Methods

| Method                    | Type                                 |
|---------------------------|--------------------------------------|
| `#filtersControl`         | `(): void`                           |
| `#linksHandler`           | `(e: any, scrollUp?: boolean): void` |
| `#linksHandlerWithScroll` | `(e: any): void`                     |
| `#paginationControl`      | `(): void`                           |
| `#popStateListener`       | `(): void`                           |
| `#removeListeners`        | `(): void`                           |
| `#setUpListeners`         | `(): void`                           |
| `renderCollection`        | `(params: any): void`                |
| `renderError`             | `(e?: any): void`                    |
| `scrollUp`                | `(): void`                           |
| `updateLayout`            | `(): void`                           |
| `updateLoading`           | `(isLoading?: boolean): void`        |
| `updateURL`               | `(query: any, title?: string): void` |

## Events

| Event                               | Type               |
|-------------------------------------|--------------------|
| `on:dynamic-product-search:failed`  | `CustomEvent<any>` |
| `on:dynamic-product-search:loaded`  | `CustomEvent<any>` |
| `on:dynamic-product-search:loading` | `CustomEvent<any>` |
