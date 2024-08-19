# product-form

Interactive product form

## Example

```html
<caption>Basic usage</caption>
<product-form
{% unless settings.cart_type == 'page' %}
notify-on-add
{% else %}
redirect-on-add="{{ routes.cart_url }}"
{% endunless %}
>
</product-form>
```

## Attributes

| Attribute         | Description                                |
|-------------------|--------------------------------------------|
| `notify-on-add`   | Trigger cart drawer or notification on add |
| `redirect-on-add` | Redirect to given page on add              |

## Methods

| Method        | Type                        | Description                         |
|---------------|-----------------------------|-------------------------------------|
| `removeError` | `(): void`                  | Remove error element                |
| `submit`      | `(e: Event): Promise<void>` | Submit form<br /><br />**e**: Event |
