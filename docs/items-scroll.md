# items-scroll

Items scroll

A custom element for managing and navigating a scrollable list of items,
with support for pagination, navigation controls, and responsive design.

This component automatically detects the number of items per page based on
the container width, and adjusts navigation controls accordingly.

## Example

```html
<caption>Cart recommendations</caption>
<items-scroll
class="ratio-navigation ratio-navigation-mobile"
style="--navigation-ratio: 16:9; --navigation-ratio-mobile: 4:3;"
>
<div
class="grid-layout grid-layout--3 grid-layout--1@mob"
data-items
cart-recommendations-content
></div>
</items-scroll>
```

## Attributes

| Attribute                  | Type      | Description                                      |
|----------------------------|-----------|--------------------------------------------------|
| `breakpoint-max`           | `string`  | The maximum breakpoint for enabling scroll functionality. Accepts named breakpoints or pixel values. |
| `breakpoint-min`           | `string`  | The minimum breakpoint for enabling scroll functionality. Accepts named breakpoints or pixel values. |
| `image-container-ratio`    | `string`  | Maintains the aspect ratio of images within the container. Should be a valid CSS aspect ratio value. |
| `mobile-counter-only`      | `boolean` | Displays only the navigation counter on mobile devices. |
| `page-navigation-disabled` | `boolean` | Disables the page navigation controls.           |

## Properties

| Property                                 | Attribute | Type              | Default | Description                                      |
|------------------------------------------|-----------|-------------------|---------|--------------------------------------------------|
| `breakpointMax`                          |           |                   |         |                                                  |
| `breakpointMin`                          |           |                   |         |                                                  |
| `items`                                  |           | `Element \| null` |         |                                                  |
| `navigationContainer`                    |           |                   | null    |                                                  |
| `navigationCounterOnly`                  |           | `boolean`         |         |                                                  |
| `navigationCounterSeparator`             |           | `string`          | "/"     |                                                  |
| `navigationCounterShowForPagesAmount`    |           | `number`          | 7       |                                                  |
| `navigationCounterShowUpToContainerSize` |           | `number`          | 768     |                                                  |
| `navigationNextButton`                   |           |                   | null    |                                                  |
| `navigationPrevButton`                   |           |                   | null    |                                                  |
| `pageNavigationContainer`                |           |                   | null    |                                                  |
| `pageNavigationDisabled`                 |           | `boolean`         |         |                                                  |
| `pageNavigationWrapper`                  |           |                   | null    |                                                  |
| `scrollBar`                              |           |                   |         |                                                  |
| `scrollBarTrack`                         |           |                   |         |                                                  |
| `snap`                                   | `snap`    | `string`          |         | Controls the scroll snapping behavior. Accepts 'start' or 'center'. |

## Methods

| Method              | Type                                  | Description                                      |
|---------------------|---------------------------------------|--------------------------------------------------|
| `#updateControls`   | `(): void`                            | Updates the controls of the items scroll.        |
| `smoothScrollItems` | `(position: number): Promise<number>` | Smoothly scrolls the items to a specified position.<br /><br />**position**: The target scroll position. |
