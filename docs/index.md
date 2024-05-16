## Table of Contents

| Web Component Name                 |
|--------------------------------|
| [accordion-group](#accordion-group)               |
| [announcement-bar](#announcement-bar)             |
| [back-to-top-button](#back-to-top-button)         |
| [cart-link](#cart-link)                           |
| [cart-recommendations](#cart-recommendations)     |
| [cart-store](#cart-store)                         |
| [deferred-media](#deferred-media)                 |
| [details-disclosure](#details-disclosure)         |
| [drawer-menu](#drawer-menu)                       |
| [dynamic-product-search](#dynamic-product-search) |
| [filters-dialog](#filters-dialog)                 |
| [free-shipping-bar](#free-shipping-bar)           |
| [gift-card-recipient](#gift-card-recipient)       |
| [header-container](#header-container)             |
| [header-details-disclosure](#header-details-disclosure) |
| [image-compare](#image-compare)                   |
| [image-skeleton](#image-skeleton)                 |
| [index](#index)                                   |
| [interactive-cart](#interactive-cart)             |
| [interactive-map](#interactive-map)               |
| [items-scroll](#items-scroll)                     |
| [lazy-video](#lazy-video)                         |
| [localize-details-disclosure](#localize-details-disclosure) |
| [maps-with-details](#maps-with-details)           |
| [media-carousel](#media-carousel)                 |
| [media-gallery](#media-gallery)                   |
| [modal-dialog](#modal-dialog)                     |
| [nested-menu](#nested-menu)                       |
| [pickup-availability](#pickup-availability)       |
| [popup-dialog](#popup-dialog)                     |
| [predictive-search](#predictive-search)           |
| [price-range](#price-range)                       |
| [product-card-mini](#product-card-mini)           |
| [product-card-spinner](#product-card-spinner)     |
| [product-card-swatches](#product-card-swatches)   |
| [product-form](#product-form)                     |
| [product-interactive-options](#product-interactive-options) |
| [product-model](#product-model)                   |
| [product-recommendations](#product-recommendations) |
| [product-single](#product-single)                 |
| [quantity-input](#quantity-input)                 |
| [quick-shop](#quick-shop)                         |
| [recent-searches](#recent-searches)               |
| [scroll-to-target](#scroll-to-target)             |
| [scrolling-marquee](#scrolling-marquee)           |
| [search-form](#search-form)                       |
| [search-modal](#search-modal)                     |
| [sticky-scroll](#sticky-scroll)                   |
| [tabbed-content](#tabbed-content)                 |
| [variant-selects](#variant-selects)               |
| [video-dialog](#video-dialog)                     |
| [video-gallery](#video-gallery)                   |
| [video-player](#video-player)                     |



# accordion-group

## Methods

| Method                  | Type              |
|-------------------------|-------------------|
| `#handleNonDismissible` | `(e: any): void`  |
| `#handleSingleOpen`     | `(e: any): void`  |
| `close`                 | `(id: any): void` |
| `open`                  | `(id: any): void` |


# announcement-bar

## Methods

| Method                         | Type                                         |
|--------------------------------|----------------------------------------------|
| `#createNavigation`            | `(): void`                                   |
| `#popupListener`               | `(e: any): void`                             |
| `#setUpDismissible`            | `(): void`                                   |
| `calculateSlidesWidth`         | `(): void`                                   |
| `dismiss`                      | `(): void`                                   |
| `handleIntersection`           | `(entries: any): void`                       |
| `handleScroll`                 | `(): void`                                   |
| `handleWindowResize`           | `(): void`                                   |
| `moveToSlide`                  | `(slideIndex: any, behavior?: string): void` |
| `moveToSlideById`              | `(slideId: any, behavior?: string): void`    |
| `observeMutations`             | `(): void`                                   |
| `observeSlides`                | `(): void`                                   |
| `observeSlidesText`            | `(): void`                                   |
| `resumeInteractions`           | `(): void`                                   |
| `setMaxContainerWidth`         | `(): void`                                   |
| `showNextSlide`                | `(): void`                                   |
| `showPrevSlide`                | `(): void`                                   |
| `startAutoplay`                | `(): void`                                   |
| `stopAutoplay`                 | `(): void`                                   |
| `stopInteractions`             | `(): void`                                   |
| `toggleClassBasedOnScreenSize` | `(): void`                                   |


# back-to-top-button

## Properties

| Property           |
|--------------------|
| `scrollToTop`      |
| `toggleVisibility` |

## Methods

| Method             | Type       |
|--------------------|------------|
| `scrollToTop`      | `(): void` |
| `toggleVisibility` | `(): void` |


# interactive-cart

## Methods

| Method                 | Type                   |
|------------------------|------------------------|
| `#onResize`            | `(entries: any): void` |
| `#render`              | `(): void`             |
| `#renderCart`          | `(): void`             |
| `#renderEmptyCart`     | `(): void`             |
| `#updateCartDiscounts` | `(): void`             |
| `#updateCartTotal`     | `(): void`             |
| `#updateFreeShipping`  | `(): void`             |


# cart-items


# cart-item

## Methods

| Method                          | Type                              |
|---------------------------------|-----------------------------------|
| `#changeQuantity`               | `(): Promise<void>`               |
| `#clearTotalPrice`              | `(): void`                        |
| `#removeProduct`                | `(e: any): Promise<void>`         |
| `#render`                       | `(): void`                        |
| `#renderError`                  | `(errorText?: string): void`      |
| `#renderTotalPriceAndDiscounts` | `(): void`                        |
| `#setImage`                     | `(srcsetWidths?: number[]): void` |
| `#toggleSpinner`                | `(visible?: boolean): void`       |
| `#updateSkeleton`               | `(): void`                        |


# discount-list

## Properties

| Property | Attribute |
|----------|-----------|
| `items`  | `items`   |

## Methods

| Method             | Type       |
|--------------------|------------|
| `#renderDiscounts` | `(): void` |


# cart-textarea

## Properties

| Property      |
|---------------|
| `function`    |
| `updated`     |
| `updatedHTML` |
| `updating`    |
| `value`       |


# cart-gift-wrapping-message


# cart-note


# cart-spinner


# cart-terms

## Methods

| Method          | Type                                             |
|-----------------|--------------------------------------------------|
| `#inputChange`  | `({ target: { checked } }: { target: { checked: any; }; }): void` |
| `#toggleError`  | `(visible?: boolean): void`                      |
| `#validateForm` | `(e: any): void`                                 |


# cart-notification

## Methods

| Method            | Type                              |
|-------------------|-----------------------------------|
| `#render`         | `(): void`                        |
| `#setImage`       | `(srcsetWidths?: number[]): void` |
| `#updateSkeleton` | `(): void`                        |


# cart-quantity-info

## Properties

| Property      | Type         |
|---------------|--------------|
| `infoContent` | `any \| any` |
| `itemsCount`  | `any \| any` |


# cart-gift-wrapping-banner

## Methods

| Method        | Type                                             |
|---------------|--------------------------------------------------|
| `#enable`     | `(e: any): Promise<void>`                        |
| `#setIsDoing` | `(isDoing?: boolean, error?: boolean): Promise<any>` |


# free-shipping-bar

## Methods

| Method                   | Type             |
|--------------------------|------------------|
| `#orchestrateModalEvent` | `(e: any): void` |
| `#playGoalAnimation`     | `(): void`       |
| `#setVariables`          | `(): void`       |
| `#update`                | `(): void`       |


# cart-link

## Properties

| Property     | Type         |
|--------------|--------------|
| `itemsCount` | `any \| any` |


# cart-recommendations

## Methods

| Method        | Type      |
|---------------|-----------|
| `#createCard` | `(): any` |


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
| `change`                     | `(key: string, quantity?: number \| undefined): Promise<any>` | Change cart line item<br /><br />**key**: Line item unique key<br />**quantity**: New quantity of line item |
| `clear`                      | `(): Promise<any>`                               | Clear the shopping cart                          |
| `disableCartRecommendations` | `(): Promise<void>`                              | Disable cart recommendations                     |
| `enableCartRecommendations`  | `(intent?: string \| undefined): Promise<void>`  | Enable cart recommendations<br /><br />**intent**: Recommendations intent ("related" or "complementary") |
| `getState`                   | `(): CartStoreObject`                            | Get current cart store state                     |
| `refresh`                    | `(): Promise<any>`                               | Refresh cart                                     |
| `resetLatestAddedProduct`    | `(): Promise<void>`                              | Reset latest added product in the store          |
| `resetVariantsBeingAdded`    | `(id?: string): Promise<void>`                   | Reset variants being added<br /><br />**id**: Variant id (if not provided, all are reset) |
| `setGiftWrapping`            | `(enable?: boolean \| undefined): Promise<any>`  | Enable or disable gift wrapping<br /><br />**enable**: undefined |
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


# deferred-media

## Methods

| Method        | Type                      |
|---------------|---------------------------|
| `loadContent` | `(focus?: boolean): void` |


# details-disclosure

## Properties

| Property            | Type         | Default              |
|---------------------|--------------|----------------------|
| `content`           | `any \| any` | "nextElementSibling" |
| `mainDetailsToggle` | `any \| any` |                      |

## Methods

| Method       | Type       |
|--------------|------------|
| `close`      | `(): void` |
| `onFocusOut` | `(): void` |
| `onToggle`   | `(): void` |


# drawer-menu

## Methods

| Method                       | Type                                             |
|------------------------------|--------------------------------------------------|
| `bindEvents`                 | `(): void`                                       |
| `closeAllOpenPanels`         | `(): void`                                       |
| `closeSubmenu`               | `(detailsElement: any, animate?: boolean): void` |
| `disableBannerHeightControl` | `(): void`                                       |
| `enableBannerHeightControl`  | `(banner: any): void`                            |
| `onCloseButtonClick`         | `(event: any): void`                             |
| `onSummaryClick`             | `(event: any): void`                             |
| `openMenuPanelById`          | `(id: any, animate?: boolean, focus?: boolean): void` |
| `openPanel`                  | `(detailsElement: any, focus?: boolean): any`    |
| `setCurrentPanelId`          | `(): void`                                       |


# dynamic-product-search

## Methods

| Method                    | Type                                 |
|---------------------------|--------------------------------------|
| `#filtersControl`         | `(): void`                           |
| `#linksHandler`           | `(e: any, scrollUp?: boolean): void` |
| `#linksHandlerWithScroll` | `(e: any): void`                     |
| `#paginationControl`      | `(): void`                           |
| `#popStateListener`       | `(): void`                           |
| `#removeListeners`        | `(): void`                           |
| `#setUpListeners`         | `(): void`                           |
| `renderCollection`        | `(params: any): void`                |
| `renderError`             | `(e?: any): void`                    |
| `scrollUp`                | `(): void`                           |
| `updateLayout`            | `(): void`                           |
| `updateLoading`           | `(isLoading?: boolean): void`        |
| `updateURL`               | `(query: any, title?: string): void` |

## Events

| Event                               | Type               |
|-------------------------------------|--------------------|
| `on:dynamic-product-search:failed`  | `CustomEvent<any>` |
| `on:dynamic-product-search:loaded`  | `CustomEvent<any>` |
| `on:dynamic-product-search:loading` | `CustomEvent<any>` |


# filters-dialog

## Methods

| Method                    | Type                      |
|---------------------------|---------------------------|
| `#handleMediaQueryChange` | `(e: any): Promise<void>` |
| `destroy`                 | `(): void`                |
| `init`                    | `(): void`                |


# gift-card-recipient

## Properties

| Property   | Type                  |
|------------|-----------------------|
| `checkbox` | `any \| any`          |
| `fields`   | `NodeListOf<Element>` |
| `fieldset` | `any \| any`          |

## Methods

| Method             | Type       |
|--------------------|------------|
| `activateFieldset` | `(): void` |


# header-container

## Methods

| Method             | Type                                        |
|--------------------|---------------------------------------------|
| `#hasScrolled`     | `(navbarHeight: any, delta?: number): void` |
| `#setScrollStatus` | `(didScroll?: boolean): void`               |


# header-details-disclosure

## Methods

| Method                 | Type                       |
|------------------------|----------------------------|
| `#disableSummaryLink`  | `(): void`                 |
| `#enableSummaryLink`   | `(): void`                 |
| `#removeContentHeight` | `(): void`                 |
| `#setContentHeight`    | `(padding?: number): void` |
| `close`                | `(): void`                 |
| `disableListeners`     | `(): void`                 |
| `mouseEnterListener`   | `(): void`                 |
| `mouseLeaveListener`   | `(): void`                 |
| `onToggle`             | `(): void`                 |
| `open`                 | `(): void`                 |


# image-compare


# image-skeleton

## Methods

| Method         | Type       |
|----------------|------------|
| `init`         | `(): void` |
| `markAsLoaded` | `(): void` |


# interactive-map


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


# lazy-video


# localize-details-disclosure

## Methods

| Method         | Type             |
|----------------|------------------|
| `#handleClick` | `(e: any): void` |


# maps-with-details

## Methods

| Method      | Type                   |
|-------------|------------------------|
| `#onResize` | `(entries: any): void` |


# media-carousel

Media carousel

## Example

```html
<caption>Basic usage</caption>
<media-carousel
id="unique-media-carousel-id"
class="
media-gallery__slider
swiper
"
data-virtual="true"
data-initial-slide="8"
data-navigation="true"
>
<media-carousel-slider class="swiper">
<media-carousel-wrapper class="swiper-wrapper">
<!-- Not required in virtual mode -->
<media-carousel-slide class="swiper-slide">...</media-carousel-slide>
...
</media-carousel-wrapper>
</media-carousel-slider>

<button
class="
media-gallery__arrow
media-gallery__arrow--prev
js-carousel-prev
"
>
<i class="icon icon--left"></i>
</button>
<button
class="
media-gallery__arrow
media-gallery__arrow--next
js-carousel-next
"
>
<i class="icon icon--right"></i>
</button>

<!-- Virtual slides -->
<div class="js-slides u-hidden-visually">
...
</div>
</media-carousel>
```

## Attributes

| Attribute             | Type      | Description                                      |
|-----------------------|-----------|--------------------------------------------------|
| `data-auto-height`    | `Boolean` | Enable auto height                               |
| `data-autoplay`       | `Number`  | Enable autoplay with provided delay value        |
| `data-breakpoint-max` | `String`  | Only enable from the breakpoint ('phab', 'tab', 'desk') |
| `data-breakpoint-min` | `String`  | Only enable up to the breakpoint ('phab', 'tab', 'desk') |
| `data-fade`           | `Boolean` | Enable fade effect                               |
| `data-initial-slide`  | `Number`  | Initial slide                                    |
| `data-loop`           | `Boolean` | Enable loop                                      |
| `data-navigation`     | `Boolean` | Enable navigation                                |
| `data-pagination`     | `Boolean` | Enable bullets pagination                        |
| `data-space-between`  | `Number`  | Space between slides (Default: 30px)             |
| `data-speed`          | `Number`  | Animation speed (Default: 200ms)                 |
| `data-virtual`        | `Boolean` | Enable virtual slides (element with the class '.js-slides' has to be present inside the container) |

## Properties

| Property       | Modifiers | Type          | Description                 |
|----------------|-----------|---------------|-----------------------------|
| `currentSlide` | readonly  | `HTMLElement` | Get the current slide.      |
| `index`        | readonly  | `number`      | Get the current index.      |
| `initialized`  | readonly  | `boolean`     | Get the initialized status. |

## Methods

| Method                    | Type                                             | Description                                      |
|---------------------------|--------------------------------------------------|--------------------------------------------------|
| `#destroy`                | `(): void`                                       |                                                  |
| `#handleMediaQueryChange` | `(e: any): void`                                 |                                                  |
| `#init`                   | `(): void`                                       |                                                  |
| `off`                     | `(type: any, handler: any, options: any): MediaCarousel` | Remove event listener                            |
| `on`                      | `(type: any, handler: any, options: any): MediaCarousel` | Add event listener                               |
| `slideTo`                 | `(index: number, speed?: number): MediaCarousel` | Change slide<br /><br />**index**: slide index<br />**speed**: transition duration |
| `start`                   | `(): MediaCarousel`                              | Start autoplay                                   |
| `stop`                    | `(): MediaCarousel`                              | Stop autoplay                                    |

## Events

| Event                                    | Type     | Description                                  |
|------------------------------------------|----------|----------------------------------------------|
| `on:media-carousel:before-slide-change`  | `Object` | Event fired before a slide change            |
| `on:media-carousel:init`                 | `Object` | Event fired when the carousel is initialized |
| `on:media-carousel:slide-change`         | `Object` | Event fired when a slide is changed          |
| `on:media-carousel:slide-transition-end` | `Object` | Event fired after a slide transition ends    |


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


# modal-dialog

Modal component

It is important that the modal element has the descendant
element with the attribute `role="document"`, otherwise it
will fail to open. Displayed on the left by default. Assign
`modal--right` or `modal--top` classes to the element in
order to change the position of the modal. Elements with the
attribute `data-a11y-dialog-show="this-modal-id"` will be set
up to open this element on click. Elements with the attribute
`data-a11y-dialog-hide` inside the modal will be set up to close
the modal on click.

## Example

```html
<caption>Basic usage</caption>
<modal-dialog
id="unique-modal-id"
class="modal modal--right"
aria-labelledby="unique-modal-id-title"
aria-hidden="true"
>
<div class="modal__overlay" data-a11y-dialog-hide></div>
<div class="modal__wrapper" role="document">
<div class="modal__content">
<h3 id="unique-modal-id-title">Modal title</h3>
<button
title="{{ 'layout.drawers.close' | t }}"
type="button"
class="modal__close"
aria-label="{{ 'layout.drawers.close' | t }}"
data-a11y-dialog-hide
>
<i class="icon icon--close-l"></i>
</button>
...
</div>
</div>
</modal-dialog>
```

## Properties

| Property | Modifiers | Type      | Description             |
|----------|-----------|-----------|-------------------------|
| `shown`  | readonly  | `boolean` | Get modal dialog status |

## Methods

| Method           | Type                                             | Description                                      |
|------------------|--------------------------------------------------|--------------------------------------------------|
| `#onClosing`     | `(): void`                                       |                                                  |
| `#onHide`        | `(): void`                                       |                                                  |
| `#onOpening`     | `(): void`                                       |                                                  |
| `#onShow`        | `(): void`                                       |                                                  |
| `close`          | `(): Promise`                                    | Close modal                                      |
| `closeInstantly` | `(): void`                                       | Close modal instantly<br /><br />Closes modal instantly even if animations are set<br />to content element |
| `destroy`        | `(): void`                                       | Destroy modal<br /><br />Remove modal attributes abd listeners |
| `init`           | `(): void`                                       | Initialize modal<br /><br />Set up the dialog instance, assign the content element,<br />set up triggers and listeners |
| `off`            | `(type: any, handler: any, options: any): ModalDialog` | Remove event listener                            |
| `on`             | `(type: any, handler: any, options: any): ModalDialog` | Add event listener                               |
| `open`           | `(openElementAfterClose?: HTMLElement): Promise` | Open modal<br /><br />**openElementAfterClose**: Modal to open after this modal is closed |
| `openInstantly`  | `(): void`                                       | Open modal instantly<br /><br />Opens modal instantly even if animations are set<br />to content element |

## Events

| Event              | Type               | Description            |
|--------------------|--------------------|------------------------|
| `on:modal:closed`  | `CustomEvent<any>` | Modal finished closing |
| `on:modal:closing` | `CustomEvent<any>` | Modal started closing  |
| `on:modal:opened`  | `CustomEvent<any>` | Modal finished opening |
| `on:modal:opening` | `CustomEvent<any>` | Modal started opening  |

## CSS Custom Properties

| Property                   | Description                           |
|----------------------------|---------------------------------------|
| `--background-color`       | Modal background color                |
| `--close-button-font-size` | Close button icon size                |
| `--close-button-size`      | Close button size                     |
| `--closing-speed`          | Modal closing speed                   |
| `--color`                  | Modal text color                      |
| `--opening-speed`          | Modal opening speed                   |
| `--width`                  | Modal width (if placed right or left) |


# nested-menu

## Properties

| Property           | Type               |
|--------------------|--------------------|
| `menu`             | `any \| any`       |
| `rows`             | `array`            |
| `submenuDirection` | `string`           |
| `submenus`         | `array`            |
| `tolerance`        | `string \| number` |

## Methods

| Method                | Type                                  | Description                                      |
|-----------------------|---------------------------------------|--------------------------------------------------|
| `#activationDelay`    | `(): number`                          | Return the amount of time that should be used as a delay before the<br />currently hovered row is activated.<br /><br />Returns 0 if the activation should happen immediately. Otherwise,<br />returns the number of milliseconds that should be delayed before<br />checking again to see if the row should be activated. |
| `#clickRow`           | `(e: any): void`                      | Immediately activate a row if the user clicks on it. |
| `#mouseenterRow`      | `(e: any): void`                      | Trigger a possible row activation whenever entering a new row. |
| `#mouseleaveMenu`     | `(): void`                            | Cancel possible row activations when leaving the menu entirely |
| `#mousemoveDocument`  | `(e: any): void`                      | Keep track of the last few locations of the mouse. |
| `#possiblyActivate`   | `(row: any): void`                    | Possibly activate a menu row. If mouse movement indicates that we<br />shouldn't activate yet because user may be trying to enter<br />a submenu's content, then delay and check again later. |
| `#possiblyDeactivate` | `(row: any, initialDelay: any): void` | Possibly deactivate a menu row. If mouse movement indicates that we<br />shouldn't deactivate yet because user may be trying to enter<br />a submenu's content, then delay and check again later. |
| `activate`            | `(row: any): void`                    | Activate a menu row.                             |


# pickup-availability

## Methods

| Method               | Type                            |
|----------------------|---------------------------------|
| `fetchAvailability`  | `(variantId: any): void`        |
| `onClickRefreshList` | `(): void`                      |
| `renderError`        | `(): void`                      |
| `renderPreview`      | `(sectionInnerHTML: any): void` |


# popup-dialog

Popup dialog

It is important that the popup element has the descendant
element with the attribute `role="document"`, otherwise it
will fail to open. Displayed in the center by default. Assign
`popup--full`, `popup--top`, `popup--right`, `popup--bottom` or `popup--left`
classes to the element in order to change the position of the popup.
Omit `<div class="popup__overlay"></div>` if you want the popup to
be transparent. Elements with the attribute data-a11y-dialog-show="this-modal-id"
will be set up to open this element on click. Elements with the attribute
data-a11y-dialog-hide inside the popup will be set up to close
the popup on click.

## Example

```html
<caption>Basic usage</caption>
<popup-dialog
id="unique-popup-id"
class="
popup
popup--full
"
data-disable-body-scroll
data-open-on-page-load="1000"
data-remember-state="14"
aria-hidden="true"
aria-labelledby="unique-popup-title"
role="ariadialog"
>
<div class="popup__overlay"></div>
<div class="popup__wrapper">
<div class="popup__content" role="document">
<h3 id="unique-popup-title">Popup title</h3>
<button
title="{{ 'layout.drawers.close' | t }}"
type="button"
class="popup__close"
aria-label="{{ 'layout.drawers.close' | t }}"
data-a11y-dialog-hide
>
<i class="icon icon--close-l"></i>
</button>
...
</div>
</div>
</popup-dialog>
```

## Attributes

| Attribute                     | Description                                      |
|-------------------------------|--------------------------------------------------|
| `data-disable-body-scroll`    | Disable body scrolling                           |
| `data-dismiss-after-interval` | Dismiss the dialog after<br />the specified interval in milliseconds |
| `data-open-on-page-load`      | Open the dialog on page<br />load. Optional delay can be provided in milliseconds |
| `data-remember-state`         | Remember the dialog state<br />on popup close. Optional cookie expiry date in days<br />can be provided, otherwise session cookie is created |
| `role`                        | Popup role. Id set to "alertdialog", hitting<br />"Escape" key will not dismiss it |

## Properties

| Property | Modifiers | Type      | Description             |
|----------|-----------|-----------|-------------------------|
| `shown`  | readonly  | `boolean` | Get popup dialog status |

## Methods

| Method           | Type                                             | Description                                      |
|------------------|--------------------------------------------------|--------------------------------------------------|
| `#onClosing`     | `(): void`                                       |                                                  |
| `#onHide`        | `(): void`                                       |                                                  |
| `#onMouseEnter`  | `(): void`                                       |                                                  |
| `#onMouseLeave`  | `(): void`                                       |                                                  |
| `#onOpening`     | `(): void`                                       |                                                  |
| `#onShow`        | `(): void`                                       |                                                  |
| `close`          | `(): Promise`                                    | Close popup                                      |
| `closeInstantly` | `(): void`                                       | Close popup instantly<br /><br />Closes popup instantly even if animations are set<br />to content element |
| `off`            | `(type: any, handler: any, options: any): PopupDialog` | Remove event listener                            |
| `on`             | `(type: any, handler: any, options: any): PopupDialog` | Add event listener                               |
| `open`           | `(): Promise`                                    | Open modal                                       |
| `openInstantly`  | `(): void`                                       | Open popup instantly<br /><br />Opens popup instantly even if animations are set<br />to content element |

## Events

| Event              | Type               | Description            |
|--------------------|--------------------|------------------------|
| `on:popup:closed`  | `CustomEvent<any>` | Popup finished closing |
| `on:popup:closing` | `CustomEvent<any>` | Popup started closing  |
| `on:popup:opened`  | `CustomEvent<any>` | Popup finished opening |
| `on:popup:opening` | `CustomEvent<any>` | Popup started opening  |

## CSS Custom Properties

| Property                   | Description            |
|----------------------------|------------------------|
| `--background-color`       | Popup background color |
| `--close-button-font-size` | Close button icon size |
| `--close-button-size`      | Close button size      |
| `--closing-speed`          | Popup closing speed    |
| `--color`                  | Popup text color       |
| `--opening-speed`          | Popup opening speed    |
| `--width`                  | Popup max width        |


# predictive-search

## Properties

| Property     | Type            |
|--------------|-----------------|
| `isDropdown` | `boolean`       |
| `type`       | `string \| any` |

## Methods

| Method                       | Type                          |
|------------------------------|-------------------------------|
| `#addSpinner`                | `(): void`                    |
| `#onChange`                  | `(): void`                    |
| `#onFocus`                   | `(): void`                    |
| `#onFocusOut`                | `(): void`                    |
| `#onKeyup`                   | `(event: any): void`          |
| `#onResultsClick`            | `(e: any): void`              |
| `#setDrawerContentMaxHeight` | `(): void`                    |
| `#updateLoading`             | `(isLoading?: boolean): void` |
| `close`                      | `(): void`                    |
| `getQuery`                   | `(): any`                     |
| `getSearchResults`           | `(searchTerm: any): void`     |
| `open`                       | `(): void`                    |
| `selectOption`               | `(): void`                    |
| `switchOption`               | `(direction: any): void`      |


# price-range

## Methods

| Method           | Type       |
|------------------|------------|
| `#onNumberInput` | `(): void` |
| `#onRangeInput`  | `(): void` |


# product-card-spinner

## Properties

| Property       | Type     | Default   |
|----------------|----------|-----------|
| `loadingClass` | `string` | "loading" |

## Methods

| Method             | Type                        |
|--------------------|-----------------------------|
| `#handleImageLoad` | `(mutationList: any): void` |
| `#init`            | `(): void`                  |


# product-card-swatches

## Properties

| Property      | Type                  |
|---------------|-----------------------|
| `hoverImage`  | `any \| any`          |
| `image`       | `any \| any`          |
| `product`     | `any \| any`          |
| `productLink` | `any \| any`          |
| `triggers`    | `NodeListOf<Element>` |

## Methods

| Method                   | Type                     |
|--------------------------|--------------------------|
| `updateCardImage`        | `(swatch: any): boolean` |
| `updateQuickShopVariant` | `(swatch: any): void`    |


# product-card-mini

## Properties

| Property  | Type             |
|-----------|------------------|
| `id`      | `string \| null` |
| `product` |                  |

## Methods

| Method                     | Type                                             |
|----------------------------|--------------------------------------------------|
| `#onQuickShopTriggerClick` | `(event: any): Promise<void>`                    |
| `renderImage`              | `(url: any, width: any, height: any, classes?: string, alt?: string, sizes?: string, srcsetWidths?: number[]): HTMLImageElement \| null` |
| `updateImage`              | `(url: any, width: any, height: any, alt?: string, srcsetWidths?: number[]): void` |
| `updateSkeleton`           | `(): void`                                       |


# product-card

## Properties

| Property  | Type             |
|-----------|------------------|
| `id`      | `string \| null` |
| `product` |                  |

## Methods

| Method                     | Type                                             |
|----------------------------|--------------------------------------------------|
| `#onQuickShopTriggerClick` | `(event: any): Promise<void>`                    |
| `#removeSwatchesListeners` | `(): void`                                       |
| `#setProductData`          | `(): void`                                       |
| `#setUpSwatchesListeners`  | `(): void`                                       |
| `renderImage`              | `(url: any, width: any, height: any, classes?: string, alt?: string, sizes?: string, srcsetWidths?: number[]): HTMLImageElement \| null` |
| `setVariant`               | `(e: any): void`                                 |
| `updateImage`              | `(url: any, width: any, height: any, alt?: string, srcsetWidths?: number[]): void` |
| `updateSkeleton`           | `(): void`                                       |


# product-form

## Methods

| Method         | Type                                             |
|----------------|--------------------------------------------------|
| `#renderError` | `(message: any): void`                           |
| `#setIsAdding` | `(isAdding?: boolean, error?: boolean): Promise<any>` |
| `removeError`  | `(): void`                                       |
| `submit`       | `(e: any): Promise<void>`                        |


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


# product-model

## Methods

| Method               | Type                  |
|----------------------|-----------------------|
| `loadContent`        | `(): void`            |
| `setupModelViewerUI` | `(errors: any): void` |

## Events

| Event                     | Type               |
|---------------------------|--------------------|
| `on:product-model:loaded` | `CustomEvent<any>` |


# product-recommendations

## Properties

| Property      | Type     | Default |
|---------------|----------|---------|
| `fetch_delay` | `number` | 0       |

## Methods

| Method                 | Type       |
|------------------------|------------|
| `#loadRecommendations` | `(): void` |


# product-single

## Properties

| Property  |
|-----------|
| `variant` |

## Methods

| Method                                 | Type       |
|----------------------------------------|------------|
| `#moveModalsFromStickyScrollContainer` | `(): void` |
| `updateMedia`                          | `(): void` |


# quantity-input

## Properties

| Property | Type     |
|----------|----------|
| `value`  | `number` |

## Methods

| Method     | Type             |
|------------|------------------|
| `add`      | `(): void`       |
| `subtract` | `(): void`       |
| `validate` | `(e: any): void` |

## Events

| Event    | Type                           |
|----------|--------------------------------|
| `update` | `CustomEvent<{ value: any; }>` |


# quick-shop

## Properties

| Property    |
|-------------|
| `variantId` |

## Methods

| Method                       | Type                                             |
|------------------------------|--------------------------------------------------|
| `#fetchQuickShop`            | `(): Promise<void>`                              |
| `#fetchQuickShopOnProximity` | `(entries: any, observer: any): Promise<void>`   |
| `#onCloseModal`              | `(): void`                                       |
| `#onOpenModal`               | `(): void`                                       |
| `#onVariantChange`           | `(event: any): void`                             |
| `#removeFetchListeners`      | `(): void`                                       |
| `#setProductData`            | `(): void`                                       |
| `#setUpFetchListeners`       | `(): void`                                       |
| `#updateContent`             | `(newContent: any): void`                        |
| `#updateImage`               | `(url: any, width: any, height: any, alt?: string, srcsetWidths?: number[]): void` |
| `#updateVariant`             | `(): void`                                       |
| `close`                      | `(): Promise<any>`                               |

## Events

| Event                   | Type               |
|-------------------------|--------------------|
| `on:quick-shop:failed`  | `CustomEvent<any>` |
| `on:quick-shop:loaded`  | `CustomEvent<any>` |
| `on:quick-shop:loading` | `CustomEvent<any>` |


# recent-searches


# scroll-to-target


# scrolling-marquee

## Properties

| Property           | Type            | Default       |
|--------------------|-----------------|---------------|
| `marqueeContainer` | `any \| any`    |               |
| `marqueeElements`  | `array`         | [null]        |
| `marqueeSpeed`     | `string \| any` |               |
| `marqueeWidth`     |                 | "offsetWidth" |
| `resizeObserver`   |                 |               |
| `speed`            | `number`        |               |
| `speedModifier`    | `number`        | 10            |

## Methods

| Method            | Type       |
|-------------------|------------|
| `observeMarquee`  | `(): void` |
| `setMarqueeSpeed` | `(): void` |


# search-form

## Properties

| Property | Type         |
|----------|--------------|
| `form`   | `any \| any` |

## Methods

| Method                         | Type       |
|--------------------------------|------------|
| `addFormStateToRecentSearches` | `(): void` |


# search-modal

## Methods

| Method                | Type       |
|-----------------------|------------|
| `#onCloseSearchModal` | `(): void` |


# sticky-scroll

## Methods

| Method                   | Type       |
|--------------------------|------------|
| `#setStickyDisplacement` | `(): void` |
| `#setStyles`             | `(): void` |
| `#setTopGap`             | `(): void` |


# tabbed-content

## Methods

| Method    | Type              |
|-----------|-------------------|
| `openTab` | `(id: any): void` |


# tab-triggers

## Properties

| Property     | Type     |
|--------------|----------|
| `alignItems` | `string` |

## Methods

| Method                  | Type       |
|-------------------------|------------|
| `#initLinkUpdate`       | `(): void` |
| `#initTriggersObserver` | `(): void` |
| `#moveToSelected`       | `(): void` |
| `#updateControls`       | `(): void` |


# variant-selects

## Methods

| Method                     | Type                                       |
|----------------------------|--------------------------------------------|
| `getVariantData`           | `(): any`                                  |
| `onVariantChange`          | `(): void`                                 |
| `removeErrorMessage`       | `(): void`                                 |
| `renderProductInfo`        | `(): void`                                 |
| `setUnavailable`           | `(): void`                                 |
| `toggleAddButton`          | `(disable?: boolean, text?: string): void` |
| `updateMasterId`           | `(): void`                                 |
| `updateOptions`            | `(): void`                                 |
| `updatePickupAvailability` | `(): void`                                 |
| `updateURL`                | `(): void`                                 |
| `updateVariantInput`       | `(): void`                                 |

## Events

| Event               | Type                             |
|---------------------|----------------------------------|
| `change`            |                                  |
| `on:variant:change` | `CustomEvent<{ variant: any; }>` |


# variant-radios

## Methods

| Method                     | Type                                       |
|----------------------------|--------------------------------------------|
| `getVariantData`           | `(): any`                                  |
| `onVariantChange`          | `(): void`                                 |
| `removeErrorMessage`       | `(): void`                                 |
| `renderProductInfo`        | `(): void`                                 |
| `setUnavailable`           | `(): void`                                 |
| `toggleAddButton`          | `(disable?: boolean, text?: string): void` |
| `updateMasterId`           | `(): void`                                 |
| `updateOptions`            | `(): void`                                 |
| `updatePickupAvailability` | `(): void`                                 |
| `updateURL`                | `(): void`                                 |
| `updateVariantInput`       | `(): void`                                 |

## Events

| Event               | Type                             |
|---------------------|----------------------------------|
| `change`            |                                  |
| `on:variant:change` | `CustomEvent<{ variant: any; }>` |


# variant-swatches

## Methods

| Method        | Type       |
|---------------|------------|
| `updateLabel` | `(): void` |


# variant-mixed-inputs

## Methods

| Method                     | Type                                       |
|----------------------------|--------------------------------------------|
| `getVariantData`           | `(): any`                                  |
| `onVariantChange`          | `(): void`                                 |
| `removeErrorMessage`       | `(): void`                                 |
| `renderProductInfo`        | `(): void`                                 |
| `setUnavailable`           | `(): void`                                 |
| `toggleAddButton`          | `(disable?: boolean, text?: string): void` |
| `updateMasterId`           | `(): void`                                 |
| `updateOptions`            | `(): void`                                 |
| `updatePickupAvailability` | `(): void`                                 |
| `updateURL`                | `(): void`                                 |
| `updateVariantInput`       | `(): void`                                 |

## Events

| Event               | Type                             |
|---------------------|----------------------------------|
| `change`            |                                  |
| `on:variant:change` | `CustomEvent<{ variant: any; }>` |


# video-dialog

Video popup dialog

Load and plays the video when opened, pauses on close
Inherits all the methods and events of PopupDialog class

## Example

```html
<caption>Basic usage</caption>
<video-dialog
id="video-dialog-unique-id"
class="
popup
popup--video
"
data-disable-body-scroll
aria-hidden="true"
>
<div class="popup__overlay" data-a11y-dialog-hide></div>

<div class="popup__wrapper">
<button
title="{{ 'layout.drawers.close' | t }}"
type="button"
class="popup__close"
aria-label="{{ 'layout.drawers.close' | t }}"
data-a11y-dialog-hide
>
<i class="icon icon--close-l"></i>
</button>
<div
class="popup__content"
role="document"
>
{% raw %}
{% render 'video-player',
id: video_player_id,
video_type: 'html5',
video: video_file,
poster_image_sizes: '(min-width: 990px) 990px, calc(100vw - 36px)'
%}
{% endraw %}
</div>
</div>
</video-dialog>
```

## Methods

| Method              | Type       |
|---------------------|------------|
| `#loadVideoAndPlay` | `(): void` |
| `#pauseVideo`       | `(): void` |


# video-gallery

Video gallery

## Example

```html
<caption>Basic usage</caption>
<video-gallery>
<video-gallery-stage class="home-video__stage">
<div class="o-ratio o-ratio--16:9">
<div class="o-ratio__content">
<video-gallery-slide
 class="home-video__stage-video is-active"
 id="video-gallery-slide--1"
>
 {% raw %}
 {% render 'video-player',
   id: 'video-player-1',
   video_type: "youtube",
   external_video_id: "1234567789",
   poster_image: preview_image_object,
   poster_image_sizes: '(min-width: 1200px) 1200px, calc(100vw - 36px)'
 %}
 {% endraw %}
</video-gallery-slide>
<video-gallery-slide
 class="home-video__stage-video"
 id="video-gallery-slide--2"
>
 {% raw %}
 {% render 'video-player',
   id: 'video-player-2',
   video_type: "vimeo",
   external_video_id: "1234567789",
   poster_image_sizes: '(min-width: 1200px) 1200px, calc(100vw - 36px)'
 %}
 {% endraw %}
</video-gallery-slide>
<video-gallery-slide
 class="home-video__stage-video"
 id="video-gallery-slide--3"
>
 {% raw %}
 {% render 'video-player',
   id: 'video-player-1',
   video_type: 'html5',
   video: video,
   poster_image_sizes: '(min-width: 1200px) 1200px, calc(100vw - 36px)'
 %}
 {% endraw %}
</video-gallery-slide>
</div>
</div>
</video-gallery-stage>

<video-gallery-thumbnails class="home-video__items">
<video-gallery-thumbnail class="home-video__item is-active">
<button
type="button"
class="home-video__item-link"
data-target-id="video-gallery-slide--{{ block.id }}"
>
<div class="o-ratio o-ratio--16:9">
 <div class="o-ratio__content">
   <img
     class="home-video__item-img"
     src="https://img.youtube.com/vi/[external_video_id]/mqdefault.jpg"
     alt="Video 1 trigger image"
     loading="lazy"
   >
   <div class="home-video__item-img--overlay u-bg-overlay"></div>
   <div class="home-video__item-icon home-video__item-icon--play u-flex u-flex--middle u-flex--center icon-fallback">
     <i class="icon icon--play" aria-hidden="true"></i>
     <span class="icon-fallback__text">{{ 'sections.video.play_label' | t }}</span>
   </div>
 </div>
</div>
</button>
</video-gallery-thumbnail>
<video-gallery-thumbnail class="home-video__item">
<button
type="button"
class="home-video__item-link"
data-target-id="video-gallery-slide--2"
>
<div class="o-ratio o-ratio--16:9">
 <div class="o-ratio__content">
   <img
     class="home-video__item-img js-vimeo-thumb"
     src="#"
     alt="Video 2 trigger image"
     loading="lazy"
     data-vimeo-id="123456789"
     style="opacity: 0"
   >
   <div class="home-video__item-img--overlay u-bg-overlay"></div>
   <div class="home-video__item-icon home-video__item-icon--play u-flex u-flex--middle u-flex--center icon-fallback">
     <i class="icon icon--play" aria-hidden="true"></i>
     <span class="icon-fallback__text">{{ 'sections.video.play_label' | t }}</span>
   </div>
 </div>
</div>
</button>
</video-gallery-thumbnail>
<video-gallery-thumbnail class="home-video__item is-active">
<button
type="button"
class="home-video__item-link"
data-target-id="video-gallery-slide--{{ block.id }}"
>
<div class="o-ratio o-ratio--16:9">
 <div class="o-ratio__content">
   <img
     class="home-video__item-img"
     src="{{ video_file.preview_image | image_url: width: 300 }}"
     alt="Video 3 trigger image"
     loading="lazy"
     width="300"
   >
   <div class="home-video__item-img--overlay u-bg-overlay"></div>
   <div class="home-video__item-icon home-video__item-icon--play u-flex u-flex--middle u-flex--center icon-fallback">
     <i class="icon icon--play" aria-hidden="true"></i>
     <span class="icon-fallback__text">{{ 'sections.video.play_label' | t }}</span>
   </div>
 </div>
</div>
</button>
</video-gallery-thumbnail>
</video-gallery-thumbnails>
</video-gallery>
```

## Methods

| Method         | Type                                  | Description                                      |
|----------------|---------------------------------------|--------------------------------------------------|
| `#handleClick` | `(e: any): void`                      |                                                  |
| `changeSlide`  | `(videSlideId: number): VideoGallery` | Change slide<br /><br />**videSlideId**: ID of the target slide |


# video-gallery-thumbnail

## Methods

| Method                  | Type                |
|-------------------------|---------------------|
| `#updateVimeoThumbnail` | `(): Promise<void>` |


# video-player

Video player

## Example

```html
<caption>Basic usage</caption>
<video-player
data-type="youtube"
data-poster="{{ media.preview_image | image_url: width: 1946 }}"
style="--aspect-ratio: {{ media.preview_image.width }} / {{ media.preview_image.height }}""
>
<video-poster>
{{ media.preview_image | image_url: width: 1946 | image_tag:
loading: lazy,
sizes: sizes,
widths: '246, 493, 600, 713, 823, 990, 1100, 1206, 1346, 1426, 1646, 1946'
}}
</video-poster>
{% raw %}
{% render 'theme-spinner', tag: 'video-loading-indicator', hidden: true %}
{% endraw %}
<video-element></video-element>
<template>
<div id="{{ section.id | append: '--' | append: media.id }}" video-element data-{{- media.host -}}-id="{{ media.external_id }}"></div>
<!-- for native video
<video video-element src="media.sources[0].url"></video>
-->
</template>
</video-player>
```

## Attributes

| Attribute     | Description                                      |
|---------------|--------------------------------------------------|
| `data-poster` | Poster (Optional: useful for external videos to replace the default one) |
| `data-type`   | Video type ("html5", "youtube", "vimeo")         |

## Properties

| Property | Modifiers | Type      | Description             |
|----------|-----------|-----------|-------------------------|
| `ready`  | readonly  | `boolean` | Get video player status |

## Methods

| Method               | Type                                             | Description           |
|----------------------|--------------------------------------------------|-----------------------|
| `#updateVimeoPoster` | `(): Promise<void>`                              |                       |
| `loadContent`        | `(): VideoPlayer`                                | Load video content    |
| `off`                | `(type: any, handler: any, options: any): VideoPlayer` | Remove event listener |
| `on`                 | `(type: any, handler: any, options: any): VideoPlayer` | Add event listener    |
| `pause`              | `(): VideoPlayer`                                | Pause video           |
| `play`               | `(): VideoPlayer`                                | Play video            |

## Events

| Event                   | Type               | Description                |
|-------------------------|--------------------|----------------------------|
| `on:video-player:ready` | `CustomEvent<any>` | Fired when player is ready |
