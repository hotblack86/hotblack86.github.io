# dynamic-button

Dynamic button component

Used as the container with a placeholder for dynamic Shopify buttons

## Example

```html
<caption>Basic usage</caption>
<dynamic-button class="dynamic-button">
<div class="dynamic-button__placeholder skeleton-button">
<span
class="skeleton-text skeleton-text--inverse skeleton-text--small skeleton-text--inline skeleton-text--1/2"
></span>
</div>
{{ form | payment_button }}
</dynamic-button>
```
