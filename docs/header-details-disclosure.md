# header-details-disclosure

A custom element that extends DetailsDisclosure to manage header details
with additional behaviors such as animations and responsive adjustments.

## Attributes

| Attribute                 | Type      | Description                                  |
|---------------------------|-----------|----------------------------------------------|
| `adjust-mega-menu-height` | `boolean` | If set, adjusts the height of the mega menu. |

## Methods

| Method               | Type       | Description                                      |
|----------------------|------------|--------------------------------------------------|
| `close`              | `(): void` | Closes the details element and resets content alignment and height if needed. |
| `disableListeners`   | `(): void` | Removes event listeners for mouse enter and leave events from the summary element. |
| `mouseEnterListener` | `(): void` | Handles mouse enter events for the summary element to open the details. |
| `mouseLeaveListener` | `(): void` | Handles mouse leave events for the summary element to close the details. |
| `onToggle`           | `(): void` | Handles the toggle state of the details element, including animations and class updates. |
| `open`               | `(): void` | Opens the details element and adjusts content alignment and height if needed. |
