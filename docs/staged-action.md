# staged-action

Staged Action

Controls the staged action state.

## Example

```html
<caption>Basic usage</caption>
<staged-action class="staged-action">
<staged-action-text class="staged-action__text">
{{ 'products.product.add_to_cart' | t }}
</staged-action-text>
<staged-action-tick class="staged-action__tick">
<i class="icon icon--check"></i>
</staged-action-tick>
<staged-action-spinner class="staged-action__spinner">
<i class="icon icon--spinner"></i>
</staged-action-spinner>
</staged-action>
```

## Methods

| Method     | Type                        | Description                                      |
|------------|-----------------------------|--------------------------------------------------|
| `setState` | `(state?: string): Promise` | Set state<br /><br />**state**: State to set ('IDLE', 'DOING', 'DONE') |
