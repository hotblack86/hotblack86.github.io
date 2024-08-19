# dynamic-product-search

Dynamic product search

A custom web component for handling dynamic product searches,
including pagination, filtering, and URL updates.

## Example

```html
<dynamic-product-search
  data-section="products"
  data-url="https://example.com/api/products"
  data-update-url="true"
  data-page-title="Product Search"
  data-quick-shop-dynamic-checkout="true"
></dynamic-product-search>
```

## Attributes

| Attribute                          | Type     | Default | Description                                      |
|------------------------------------|----------|---------|--------------------------------------------------|
| `data-page-title`                  | `string` |         | The title of the page to set when the URL is updated. |
| `data-quick-shop-dynamic-checkout` | `string` | "false" | Enables or disables the dynamic checkout button. |
| `data-section`                     | `string` |         | The identifier for the product section.          |
| `data-update-url`                  | `string` | "true"  | Determines whether the URL should be updated when the collection changes. |
| `data-url`                         | `string` |         | The base URL for the product search API.         |

## Methods

| Method             | Type                                             | Description                                      |
|--------------------|--------------------------------------------------|--------------------------------------------------|
| `renderCollection` | `(params: { query: string; updateURL: boolean; scrollUp: boolean; }): void` | Renders a collection of products based on the provided parameters.<br />Updates the URL, scrolls the page, and manages the loading state.<br /><br />**params.query**: The query string to filter products. |
| `renderError`      | `(e?: string \| undefined): void`                | Renders an error message within the component.<br /><br />**e**: The error message to display. |
| `scrollUp`         | `(): void`                                       | Scrolls the window up to the top of the section. |
| `updateLoading`    | `(isLoading?: boolean \| undefined): void`       | Updates the loading state of the component.<br /><br />**isLoading**: Indicates whether the component is in a loading state. |
| `updateURL`        | `(query: string, title?: string): void`          | Updates the URL in the browser's history.<br /><br />**query**: The query string to append to the URL.<br />**title**: The title of the page. |

## Events

| Event                               | Type               | Description                                      |
|-------------------------------------|--------------------|--------------------------------------------------|
| `on:dynamic-product-search:failed`  | `CustomEvent<any>` | Dispatched when the product search fails to load. |
| `on:dynamic-product-search:loaded`  | `CustomEvent<any>` | Dispatched when the product search has finished loading. |
| `on:dynamic-product-search:loading` | `CustomEvent<any>` | Dispatched when the product search starts loading. |
