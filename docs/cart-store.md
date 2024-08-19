# cart-store

Cart store

Use this store to manage cart data and subscribe to changes

## Examples

```html
<caption>Add variant to cart</caption>
import Cart from 'cart-store';

const newCart = await Cart.add({
id: '123',
quantity: 1,
});
```

```html
<caption>Get cart object</caption>
import Cart from 'cart-store';

const cart = await Cart.getState().cart;
```

```html
<caption>Subscribe to cart changes</caption>
import Cart from 'cart-store';

// Subscribe to store changes
const unsubscribe = Cart.subscribe((state, prevState) => {
if (state.cart.item_count !== prevState.cart.item_count) {
console.log(state.cart.item_count);
}
});

// Clean up
unsubscribe();
```

## Methods

| Method                       | Type                                             | Description                                      |
|------------------------------|--------------------------------------------------|--------------------------------------------------|
| `#init`                      | `(): void`                                       |                                                  |
| `add`                        | `(variants: any): Promise<any>`                  | Add variant(s) to cart<br /><br />**undefined**: undefined |
| `change`                     | `({ id, quantity, properties }: CartChange): Promise<any>` | Change cart line item<br /><br />**requestBody**: Cart change request body |
| `clear`                      | `(): Promise<any>`                               | Clear the shopping cart                          |
| `disableCartRecommendations` | `(): Promise<void>`                              | Disable cart recommendations                     |
| `enableCartRecommendations`  | `(intent?: string \| undefined): Promise<void>`  | Enable cart recommendations<br /><br />**intent**: Recommendations intent ("related" or "complementary") |
| `getState`                   | `(): CartStoreObject`                            | Get current cart store state                     |
| `refresh`                    | `(): Promise<any>`                               | Refresh cart                                     |
| `resetLatestAddedProduct`    | `(): Promise<void>`                              | Reset latest added product in the store          |
| `resetVariantsBeingAdded`    | `(id?: string): Promise<void>`                   | Reset variants being added<br /><br />**id**: Variant id (if not provided, all are reset) |
| `setGiftWrapping`            | `(enable?: boolean \| undefined): Promise<any>`  | Enable or disable gift wrapping<br /><br />**enable**: undefined |
| `setState`                   | `(field: string, value: string): void`           | Set store field's value<br /><br />**field**: field name to set<br />**value**: value to set |
| `subscribe`                  | `(callback: CartStore    ~subscribeCallback): function(): void` | Subscribe to store changes<br /><br />**callback**: Callback function |
| `syncGiftWrapping`           | `(): Promise<void>`                              | Sync gift wrapping data with store settings      |
| `updateCartNote`             | `(note?: string \| undefined): Promise<any>`     | Update cart note<br /><br />**note**: Cart note  |
| `updateGiftWrappingMessage`  | `(message?: string \| undefined): Promise<any>`  | Update gift wrapping message<br /><br />**message**: Gift wrapping message |

## Events

| Event             | Type     | Description                         |
|-------------------|----------|-------------------------------------|
| `on:cart:failed`  | `Object` | Request failed event                |
| `on:cart:loaded`  | `Object` | Request finished successfully event |
| `on:cart:loading` | `Object` | Request started event               |
