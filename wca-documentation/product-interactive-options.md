# product-interactive-options

## Methods

| Method                                 | Type                                             | Description                                      |
|----------------------------------------|--------------------------------------------------|--------------------------------------------------|
| `#onChange`                            | `(e: any): void`                                 |                                                  |
| `#onClick`                             | `(e: any): void`                                 |                                                  |
| `getCurrentOptions`                    | `(): any[]`                                      |                                                  |
| `getCurrentVariant`                    | `(): any`                                        |                                                  |
| `getExistingVariantFromSelectedOption` | `(option: string, optionGroup: string): (Object \| Null)` | Get existing variant (either available or sold out) from<br />the option specified. Otherwise return null.<br /><br />**option**: Reference option<br />**optionGroup**: Option group to which the option belongs |
| `getFirstExistingVariant`              | `(option: string, optionGroup: string): (Object \| Null)` | Get the first available existing variant the option belongs to. If<br />no available variants exist, return the first existing one. Otherwise<br />return null.<br /><br />**option**: Reference option<br />**optionGroup**: Option group to which the option belongs |
| `getOptionsElementsObject`             | `(): object`                                     |                                                  |
| `getVariantById`                       | `(id: number): (Object \| Null)`                 | Get variant object by variant id<br /><br />**id**: Variant id |
| `optionsAvailableInOtherVariants`      | `(): String[]`                                   | Based on the current variant, return all options present<br />in available variants that start with the same main option<br />as the current variant, and include the same options in their<br />option list. |
| `selectCurrentOrFirstExistingVariant`  | `(option: string, optionGroup: string): void`    | Select variant if exists, otherwise select first existing one.<br /><br />**option**: Reference option<br />**optionGroup**: Option group to which the option belongs |
| `selectVariant`                        | `(variant: Object): void`                        | Set product form options to reflect the selected variant.<br /><br />**variant**: Product variant |
| `selectVariantById`                    | `(id: any): void`                                |                                                  |
| `setOptionInputsAvailability`          | `(): void`                                       | Setup product options display (available, unavailable, disabled) |
| `setUpInputListeners`                  | `(): void`                                       |                                                  |
