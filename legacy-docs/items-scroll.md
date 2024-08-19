# items-scroll

## Properties

| Property                                 | Type              | Default |
|------------------------------------------|-------------------|---------|
| `breakpointMax`                          |                   |         |
| `breakpointMin`                          |                   |         |
| `items`                                  | `Element \| null` |         |
| `navigationContainer`                    |                   | null    |
| `navigationCounterOnly`                  | `boolean`         |         |
| `navigationCounterSeparator`             | `string`          | "/"     |
| `navigationCounterShowForPagesAmount`    | `number`          | 7       |
| `navigationCounterShowUpToContainerSize` | `number`          | 768     |
| `navigationNextButton`                   |                   | null    |
| `navigationPrevButton`                   |                   | null    |
| `pageNavigationContainer`                |                   | null    |
| `pageNavigationDisabled`                 | `boolean`         |         |
| `pageNavigationWrapper`                  |                   | null    |
| `scrollBar`                              |                   |         |
| `scrollBarTrack`                         |                   |         |
| `snap`                                   | `string \| any`   |         |

## Methods

| Method                         | Type                                       |
|--------------------------------|--------------------------------------------|
| `#createNavigation`            | `(): void`                                 |
| `#disableControlsListeners`    | `(): void`                                 |
| `#enableControlsListeners`     | `(): void`                                 |
| `#getItemAtScroll`             | `(): Element`                              |
| `#handleItemsScroll`           | `(): void`                                 |
| `#handleNextNavigationAction`  | `(e: any): void`                           |
| `#handlePageNavigationClick`   | `(e: any): void`                           |
| `#handlePrevNavigationAction`  | `(e: any): void`                           |
| `#moveItems`                   | `(position: any, behavior?: string): void` |
| `#setPageNavigationState`      | `(): void`                                 |
| `#setUpItemsMutationObserver`  | `(): void`                                 |
| `#setUpNavigationStateControl` | `(): void`                                 |
| `#updateControls`              | `(): void`                                 |
| `#updatePageNavigationList`    | `(): void`                                 |
| `smoothScrollItems`            | `(position: any): Promise<any>`            |
