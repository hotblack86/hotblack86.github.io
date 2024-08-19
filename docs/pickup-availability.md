# pickup-availability

A custom web component that fetches and displays pickup availability for a given product variant.

This component checks for pickup availability based on the product variant ID and renders the appropriate information
or an error message if the data cannot be fetched.

## Example

```html
<caption>Basic usage</caption>
<pickup-availability
class="store-availability-container js"
available
data-root-url="https://example.com/"
data-variant-id="123456"
data-has-only-default-variant="false"
>
<template>
<pickup-availability-preview class="store-availability-information">
<svg class="icon icon-close"><use xlink:href="#icon-close"></use></svg>
<div class="store-availability-information-container">
<p class="store-availability-information__title">
 Pickup is currently unavailable.
</p>
<button
 type="button"
 class="store-availability-information__link store-availability-small-text link link--underline"
>
 Refresh
</button>
</div>
</pickup-availability-preview>
</template>
</pickup-availability>
```

## Attributes

| Attribute                       | Type      | Description                                      |
|---------------------------------|-----------|--------------------------------------------------|
| `available`                     | `boolean` | Determines if pickup is available.               |
| `data-has-only-default-variant` | `boolean` | Indicates if only the default variant is available. |
| `data-root-url`                 | `string`  | The root URL for fetching pickup availability.   |
| `data-variant-id`               | `string`  | The ID of the product variant to fetch availability for. |

## Methods

| Method               | Type                                    | Description                                      |
|----------------------|-----------------------------------------|--------------------------------------------------|
| `fetchAvailability`  | `(variantId: string): void`             | Fetches pickup availability data for the specified variant ID.<br /><br />**variantId**: The ID of the product variant to fetch availability for. |
| `onClickRefreshList` | `(): void`                              | Event handler for refreshing the availability list. |
| `renderError`        | `(): void`                              | Renders an error message if the availability data cannot be fetched. |
| `renderPreview`      | `(sectionInnerHTML: HTMLElement): void` | Renders the availability preview or hides the component if no availability is found.<br /><br />**sectionInnerHTML**: The inner HTML of the fetched availability section. |
