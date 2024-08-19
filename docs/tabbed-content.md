# tabbed-content

A custom web component that manages tabbed navigation and displays the corresponding tab panel content.

## Methods

| Method    | Type                 | Description                                      |
|-----------|----------------------|--------------------------------------------------|
| `openTab` | `(id: string): void` | Opens the tab with the given ID and updates the tab panels accordingly. Sets the `aria-selected` attribute on the active tab and updates visibility of tab panels. Resets any animations in the newly selected tab panel.<br /><br />**id**: The ID of the tab to open. |


# tab-triggers

A custom web component that manages the triggers for the tabs, including scrolling to the selected tab and updating external links.

## Properties

| Property     | Type     |
|--------------|----------|
| `alignItems` | `string` |
