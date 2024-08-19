# product-interactive-options

Custom HTML element that manages interactive product options.
This component handles variant selection and updates the UI to reflect
available, unavailable, and sold-out options.

## Example

```html
<caption>Usage of ProductInteractiveOptions within a variant-radios component</caption>
<variant-radios
class="js"
data-section="123456"
data-card="78910"
data-url="/products/sample-product"
data-update-url="false"
data-local-render="true"
>
<product-interactive-options>
<fieldset class="product-form__swatch">
<div class="product-form__swatch__title">
<legend>Color</legend>
</div>
<div class="product-form__swatch__item">
<input
 type="radio"
 id="unique_id-0-0"
 name="Color"
 value="Red"
 checked
>
<label for="unique_id-0-0">Red</label>
</div>
<div class="product-form__swatch__item">
<input
 type="radio"
 id="unique_id-0-1"
 name="Color"
 value="Blue"
>
<label for="unique_id-0-1">Blue</label>
</div>
</fieldset>
</product-interactive-options>
</variant-radios>
```

## Methods

| Method                                 | Type                                             | Description                                      |
|----------------------------------------|--------------------------------------------------|--------------------------------------------------|
| `getCurrentOptions`                    | `(): Array<string>`                              | Get the current options selected by the user.    |
| `getCurrentVariant`                    | `(): Object\|null`                               | Get the current variant based on the current options. |
| `getExistingVariantFromSelectedOption` | `(option: string, optionGroup: string): (Object \| Null)` | Get existing variant (either available or sold out) from<br />the option specified. Otherwise return null.<br /><br />**option**: Reference option<br />**optionGroup**: Option group to which the option belongs |
| `getFirstExistingVariant`              | `(option: string, optionGroup: string): (Object \| Null)` | Get the first available existing variant the option belongs to. If<br />no available variants exist, return the first existing one. Otherwise<br />return null.<br /><br />**option**: Reference option<br />**optionGroup**: Option group to which the option belongs |
| `getOptionsElementsObject`             | `(): Object`                                     | Creates an object containing elements of interactive product options.<br />The object is structured by option name, with each option containing an array of elements and their corresponding values. |
| `getVariantById`                       | `(id: number): (Object \| Null)`                 | Get variant object by variant id<br /><br />**id**: Variant id |
| `optionsAvailableInOtherVariants`      | `(): String[]`                                   | Based on the current variant, return all options present<br />in available variants that start with the same main option<br />as the current variant, and include the same options in their<br />option list. |
| `selectCurrentOrFirstExistingVariant`  | `(option: string, optionGroup: string): void`    | Select variant if exists, otherwise select first existing one.<br /><br />**option**: Reference option<br />**optionGroup**: Option group to which the option belongs |
| `selectVariant`                        | `(variant: Object): void`                        | Set product form options to reflect the selected variant.<br /><br />**variant**: Product variant |
| `selectVariantById`                    | `(id: number): void`                             | Selects a variant by its ID and triggers the onVariantChange event if the variant is found.<br /><br />**id**: The ID of the variant to select. |
| `setOptionInputsAvailability`          | `(): void`                                       | Setup product options display (available, unavailable, disabled) |
| `setUpInputListeners`                  | `(): void`                                       | Sets up event listeners for input elements.<br /><br />Removes the onChange event from the variant-selects or variants-radios,<br />then adds event listeners to each input element based on its type.<br />If the input type is 'inputs', a click event listener is added.<br />If the input type is 'select', a change event listener is added.<br />Finally, the onChange event is re-added to the variant-selects or variants-radios. |
