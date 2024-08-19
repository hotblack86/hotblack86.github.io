# product-recommendations

A custom element that loads product recommendations from a URL and updates the DOM with the fetched content.

## Example

```html
<caption>Basic usage</caption>
<product-recommendations
id="recommended-products"
data-url="/api/products/recommendations"
data-quick-shop-dynamic-checkout
>
</product-recommendations>
```

## Attributes

| Attribute                          | Type      | Description                                      |
|------------------------------------|-----------|--------------------------------------------------|
| `data-quick-shop-dynamic-checkout` | `boolean` | Determines if the quick shop dynamic checkout is enabled. |
| `data-url`                         | `string`  | The URL used to fetch product recommendations.   |
| `id`                               | `string`  | The unique identifier for the element.           |

## Properties

| Property      | Type     | Default |
|---------------|----------|---------|
| `fetch_delay` | `number` | 0       |
