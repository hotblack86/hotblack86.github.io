# variant-selects

A custom element that handles variant selection for products, updating the UI based on the selected variant.

## Attributes

| Attribute         | Type      | Description                                      |
|-------------------|-----------|--------------------------------------------------|
| `data-card`       | `string`  | The card identifier for the product.             |
| `data-section`    | `string`  | The section identifier for the product.          |
| `data-update-url` | `boolean` | Determines if the URL should be updated with the variant ID. |
| `data-url`        | `string`  | The URL used to update the browser history with the variant ID. |

## Methods

| Method                     | Type                                             | Description                                      |
|----------------------------|--------------------------------------------------|--------------------------------------------------|
| `getVariantData`           | `(): Array<Object>`                              | Retrieves the variant data from the JSON script tag within the element. |
| `onVariantChange`          | `(): void`                                       | Handles changes in variant selection.<br />Updates UI elements and dispatches a custom event with the selected variant. |
| `removeErrorMessage`       | `(): void`                                       | Removes any error message elements from the closest section element. |
| `renderProductInfo`        | `(): void`                                       | Renders product information such as price, unit price, label, inventory notice, and SKU. |
| `setUnavailable`           | `(): void`                                       | Sets the add-to-cart button to indicate the product is unavailable and hides the price. |
| `toggleAddButton`          | `(disable?: boolean \| undefined, text?: string \| undefined): void` | Toggles the disabled state of the add-to-cart button and updates its text.<br /><br />**disable**: Whether to disable the button.<br />**text**: The text to display on the button when disabled. |
| `updateMasterId`           | `(): void`                                       | Finds and sets the current variant based on the selected options. |
| `updateOptions`            | `(): void`                                       | Updates the selected options based on the current state of the select elements. |
| `updatePickupAvailability` | `(): void`                                       | Updates the pickup availability based on the current variant ID. |
| `updateURL`                | `(): void`                                       | Updates the URL in the browser's history with the current variant ID.<br />Does nothing if the variant is unavailable or URL updates are disabled. |
| `updateVariantInput`       | `(): void`                                       | Updates the hidden input field with the current variant ID and triggers a change event.<br />Updates the variant in the closest `product-single` element if it exists. |

## Events

| Event               | Type                             | Description                                      |
|---------------------|----------------------------------|--------------------------------------------------|
| `change`            |                                  |                                                  |
| `on:variant:change` | `CustomEvent<{ variant: any; }>` | Fired when the variant selection changes, with the current variant in the event detail. |


# variant-radios

A custom element that extends `VariantSelects` to handle variant selection using radio buttons.

## Attributes

| Attribute         | Type      | Description                                      |
|-------------------|-----------|--------------------------------------------------|
| `data-card`       | `string`  | The card identifier for the product.             |
| `data-section`    | `string`  | The section identifier for the product.          |
| `data-update-url` | `boolean` | Determines if the URL should be updated with the variant ID. |
| `data-url`        | `string`  | The URL used to update the browser history with the variant ID. |

## Methods

| Method                     | Type                                             | Description                                      |
|----------------------------|--------------------------------------------------|--------------------------------------------------|
| `getVariantData`           | `(): Array<Object>`                              | Retrieves the variant data from the JSON script tag within the element. |
| `onVariantChange`          | `(): void`                                       | Handles changes in variant selection.<br />Updates UI elements and dispatches a custom event with the selected variant. |
| `removeErrorMessage`       | `(): void`                                       | Removes any error message elements from the closest section element. |
| `renderProductInfo`        | `(): void`                                       | Renders product information such as price, unit price, label, inventory notice, and SKU. |
| `setUnavailable`           | `(): void`                                       | Sets the add-to-cart button to indicate the product is unavailable and hides the price. |
| `toggleAddButton`          | `(disable?: boolean \| undefined, text?: string \| undefined): void` | Toggles the disabled state of the add-to-cart button and updates its text.<br /><br />**disable**: Whether to disable the button.<br />**text**: The text to display on the button when disabled. |
| `updateMasterId`           | `(): void`                                       | Finds and sets the current variant based on the selected options. |
| `updateOptions`            | `(): void`                                       | Updates the selected variant options based on the checked radio inputs within fieldsets. |
| `updatePickupAvailability` | `(): void`                                       | Updates the pickup availability based on the current variant ID. |
| `updateURL`                | `(): void`                                       | Updates the URL in the browser's history with the current variant ID.<br />Does nothing if the variant is unavailable or URL updates are disabled. |
| `updateVariantInput`       | `(): void`                                       | Updates the hidden input field with the current variant ID and triggers a change event.<br />Updates the variant in the closest `product-single` element if it exists. |

## Events

| Event               | Type                             | Description                                      |
|---------------------|----------------------------------|--------------------------------------------------|
| `change`            |                                  |                                                  |
| `on:variant:change` | `CustomEvent<{ variant: any; }>` | Fired when the variant selection changes, with the current variant in the event detail. |


# variant-swatches

A custom element that handles variant selection using swatches and updates a label based on the selected variant.

## Attributes

| Attribute      | Type     | Description                                      |
|----------------|----------|--------------------------------------------------|
| `data-form-id` | `string` | The ID of the form element that contains the swatch inputs. |

## Methods

| Method        | Type       | Description                                      |
|---------------|------------|--------------------------------------------------|
| `updateLabel` | `(): void` | Updates the label based on the currently selected variant option. |


# variant-mixed-inputs

A custom element that that extends `VariantSelects` to handle variant selection using a mix of input types and select elements.

## Attributes

| Attribute         | Type      | Description                                      |
|-------------------|-----------|--------------------------------------------------|
| `data-card`       | `string`  | The card identifier for the product.             |
| `data-section`    | `string`  | The section identifier for the product.          |
| `data-update-url` | `boolean` | Determines if the URL should be updated with the variant ID. |
| `data-url`        | `string`  | The URL used to update the browser history with the variant ID. |

## Methods

| Method                     | Type                                             | Description                                      |
|----------------------------|--------------------------------------------------|--------------------------------------------------|
| `getVariantData`           | `(): Array<Object>`                              | Retrieves the variant data from the JSON script tag within the element. |
| `onVariantChange`          | `(): void`                                       | Handles changes in variant selection.<br />Updates UI elements and dispatches a custom event with the selected variant. |
| `removeErrorMessage`       | `(): void`                                       | Removes any error message elements from the closest section element. |
| `renderProductInfo`        | `(): void`                                       | Renders product information such as price, unit price, label, inventory notice, and SKU. |
| `setUnavailable`           | `(): void`                                       | Sets the add-to-cart button to indicate the product is unavailable and hides the price. |
| `toggleAddButton`          | `(disable?: boolean \| undefined, text?: string \| undefined): void` | Toggles the disabled state of the add-to-cart button and updates its text.<br /><br />**disable**: Whether to disable the button.<br />**text**: The text to display on the button when disabled. |
| `updateMasterId`           | `(): void`                                       | Finds and sets the current variant based on the selected options. |
| `updateOptions`            | `(): void`                                       | Updates the options based on the selected input and select elements.<br /><br />Collects the values of all checked input elements and all select elements within the element. |
| `updatePickupAvailability` | `(): void`                                       | Updates the pickup availability based on the current variant ID. |
| `updateURL`                | `(): void`                                       | Updates the URL in the browser's history with the current variant ID.<br />Does nothing if the variant is unavailable or URL updates are disabled. |
| `updateVariantInput`       | `(): void`                                       | Updates the hidden input field with the current variant ID and triggers a change event.<br />Updates the variant in the closest `product-single` element if it exists. |

## Events

| Event               | Type                             | Description                                      |
|---------------------|----------------------------------|--------------------------------------------------|
| `change`            |                                  |                                                  |
| `on:variant:change` | `CustomEvent<{ variant: any; }>` | Fired when the variant selection changes, with the current variant in the event detail. |
