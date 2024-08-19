# media-gallery

## Methods

| Method                               | Type                                             | Description                                      |
|--------------------------------------|--------------------------------------------------|--------------------------------------------------|
| `#adjustThumbs`                      | `(activeElement: any, behavior?: string): void`  | 1) Check if currentElement is fully or partially outside bounds<br />		outsideBefore = container.leftBound + fullElementWidth > elementOuterRightBound<br />		outsideAfter = container.rightBound - fullElementWidth < elementOuterLeftBound<br />2) Find if there is a next element after if outsideAfter or previous if outsideBefore<br />3) Move into view |
| `#calculateThumbsRatio`              | `(preferredThumbSize?: number, minContainerSize?: number): number` |                                                  |
| `#init`                              | `(): void`                                       |                                                  |
| `#initZoom`                          | `(): void`                                       |                                                  |
| `#isThumbContainerVertical`          | `(): boolean`                                    |                                                  |
| `#navigationControl`                 | `(): void`                                       |                                                  |
| `#navigationPagingVisibilityControl` | `(): void`                                       |                                                  |
| `#setCSSVars`                        | `(preferredThumbWidth?: number, preferredThumbHeight?: number): void` |                                                  |
| `#updateThumbs`                      | `({ detail: { activeIndex } }: { detail: { activeIndex: any; }; }): void` |                                                  |
| `#updateViewInSpace`                 | `({ detail: { currentSlide } }: { detail: { currentSlide: any; }; }): void` |                                                  |
| `goToSlide`                          | `(mediaId: any): void`                           |                                                  |
