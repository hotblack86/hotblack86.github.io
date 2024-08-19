# quantity-input

Custom HTML element for managing quantity input with increment and decrement buttons.
This component handles user interaction with the quantity input, including validation and updates.

## Example

```html
<caption>Basic usage</caption>
<quantity-input>
<button minus type="button" aria-label="Reduce quantity">
<span aria-hidden="true">&minus;</span>
</button>
<input
id="quantity-input"
type="number"
value="1"
min="1"
step="1"
name="quantity"
autocomplete="off"
>
<button plus type="button" aria-label="Increase quantity">
<span aria-hidden="true">+</span>
</button>
</quantity-input>
```

## Attributes

| Attribute | Type     | Description               |
|-----------|----------|---------------------------|
| `max`     | `number` | The maximum value allowed |
| `min`     | `number` | The minimum value allowed |
| `step`    | `number` | The step value            |

## Properties

| Property | Type     | Description                    |
|----------|----------|--------------------------------|
| `value`  | `number` | Sets the quantity input value. |

## Methods

| Method     | Type               | Description                                      |
|------------|--------------------|--------------------------------------------------|
| `add`      | `(): void`         | Increases the quantity value by the defined step, but not above the maximum value. |
| `subtract` | `(): void`         | Decreases the quantity value by the defined step, but not below the minimum value. |
| `validate` | `(e: Event): void` | Validates the quantity input value against the minimum and maximum constraints.<br /><br />**e**: The input change event. |

## Events

| Event    | Type          | Description                             |
|----------|---------------|-----------------------------------------|
| `update` | `CustomEvent` | Dispatched when the quantity is updated |
