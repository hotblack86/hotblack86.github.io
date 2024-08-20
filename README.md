# Table of contents

- [accordion](#accordion)
- [accordion-group](#accordion-group)
- [animations](#animations)
- [announcement-bar](#announcement-bar)
- [back-to-top-button](#back-to-top-button)
- [interactive-cart](#interactive-cart)
- [cart-items](#cart-items)
- [cart-item](#cart-item)
- [discount-list](#discount-list)
- [cart-text-input](#cart-text-input)
- [cart-gift-wrapping-message](#cart-gift-wrapping-message)
- [cart-note](#cart-note)
- [cart-terms](#cart-terms)
- [cart-notification](#cart-notification)
- [cart-quantity-info](#cart-quantity-info)
- [cart-gift-wrapping-banner](#cart-gift-wrapping-banner)
- [free-shipping-bar](#free-shipping-bar)
- [cart-link](#cart-link)
- [cart-recommendations](#cart-recommendations)
- [cart-store](#cart-store)
- [deferred-media](#deferred-media)
- [details-disclosure](#details-disclosure)
- [drawer-menu](#drawer-menu)
- [dynamic-button](#dynamic-button)
- [dynamic-product-search](#dynamic-product-search)
- [filters-dialog](#filters-dialog)
- [gift-card-recipient](#gift-card-recipient)
- [header-container](#header-container)
- [header-details-disclosure](#header-details-disclosure)
- [image-compare](#image-compare)
- [image-skeleton](#image-skeleton)
- [interactive-map](#interactive-map)
- [items-scroll](#items-scroll)
- [lazy-video](#lazy-video)
- [localize-details-disclosure](#localize-details-disclosure)
- [maps-with-details](#maps-with-details)
- [media-carousel](#media-carousel)
- [media-gallery](#media-gallery)
- [modal-dialog](#modal-dialog)
- [nested-menu](#nested-menu)
- [pickup-availability](#pickup-availability)
- [popup-dialog](#popup-dialog)
- [predictive-search](#predictive-search)
- [price-range](#price-range)
- [product-card-spinner](#product-card-spinner)
- [product-card-swatches](#product-card-swatches)
- [product-card-mini](#product-card-mini)
- [product-card](#product-card)
- [product-form](#product-form)
- [product-interactive-options](#product-interactive-options)
- [product-model](#product-model)
- [product-recommendations](#product-recommendations)
- [product-single](#product-single)
- [quantity-input](#quantity-input)
- [quick-shop](#quick-shop)
- [recent-searches](#recent-searches)
- [scroll-to-target](#scroll-to-target)
- [scrolling-marquee](#scrolling-marquee)
- [search-form](#search-form)
- [search-modal](#search-modal)
- [staged-action](#staged-action)
- [sticky-scroll](#sticky-scroll)
- [tabbed-content](#tabbed-content)
- [tab-triggers](#tab-triggers)
- [variant-selects](#variant-selects)
- [variant-radios](#variant-radios)
- [variant-swatches](#variant-swatches)
- [variant-mixed-inputs](#variant-mixed-inputs)
- [video-dialog](#video-dialog)
- [video-gallery](#video-gallery)
- [video-gallery-thumbnail](#video-gallery-thumbnail)
- [video-player](#video-player)


# accordion

Accordion class to handle the opening and closing of a single accordion item.

## Properties

| Property      | Type         | Default |
|---------------|--------------|---------|
| `animation`   |              | null    |
| `content`     | `any \| any` |         |
| `el`          |              | "el"    |
| `isClosing`   | `boolean`    | false   |
| `isExpanding` | `boolean`    | false   |
| `summary`     | `any \| any` |         |

## Methods

| Method              | Type                    | Description                                      |
|---------------------|-------------------------|--------------------------------------------------|
| `expand`            | `(): void`              | Expands the accordion with an animation.         |
| `onAnimationFinish` | `(open: boolean): void` | Finishes the animation and resets the state of the accordion.<br /><br />**open**: Whether the accordion should be open. |
| `onClick`           | `(e: MouseEvent): void` | Handles the click event on the accordion summary element.<br /><br />**e**: The click event. |
| `open`              | `(): void`              | Opens the accordion.                             |
| `shrink`            | `(): void`              | Initiates the closing animation of the accordion. |

## Events

| Event                    | Type               | Description                                    |
|--------------------------|--------------------|------------------------------------------------|
| `on:accordion:cancelled` | `CustomEvent<any>` | Fires when an ongoing animation is canceled.   |
| `on:accordion:closed`    | `CustomEvent<any>` | Fires when the accordion has finished closing. |
| `on:accordion:closing`   | `CustomEvent<any>` | Fires when the accordion begins to close.      |
| `on:accordion:opened`    | `CustomEvent<any>` | Fires when the accordion has finished opening. |
| `on:accordion:opening`   | `CustomEvent<any>` | Fires when the accordion begins to open.       |


# accordion-group

AccordionGroup class to manage multiple accordions within a group.

## Attributes

| Attribute    | Type      | Description                                      |
|--------------|-----------|--------------------------------------------------|
| `alwaysOpen` | `boolean` | If true, ensures at least one accordion is always open. |
| `singleOpen` | `boolean` | If true, only one accordion in the group can be open at a time. |

## Methods

| Method  | Type                 | Description                                      |
|---------|----------------------|--------------------------------------------------|
| `close` | `(id: string): void` | Closes the accordion with the given ID.<br /><br />**id**: The ID of the accordion to close. |
| `open`  | `(id: string): void` | Opens the accordion with the given ID.<br /><br />**id**: The ID of the accordion to open. |


# animations

Animations

Set up and reset theme animations. In order to set up animations on
the element, use `js-animate-single` or `js-animate-sequence` classes
with these attributes to amend default parameters:
- `data-animation-delay`: Animation delay in seconds
- `data-animation-displacement`: Element displacement in pixels (Default: 10)
- `data-animation-duration`: Animation duration in seconds (Default: 0.5)
- `data-animation-interval`: Animation interval in seconds (Default: ANIMATION_INTERVAL from store-data.js.liquid)
- `data-animation-replay`: Replay animation when element gets back into view
- `data-animation-scale`: Element scale as ratio
- `data-animation-selector`: Descendant elements selector (children by default)
In order to set up complex animations, where animations are different
for each selector, use `js-animate-sequence` with `data-animation`, and
pass it a json array of objects with the parameters listed above as keys,
omitting 'data-animation', like so:
[
 {"delay": 0.5, "selector": ".element-class-one", ...},
 {"delay": 0.15, "selector": ".element-class-two", ...}
]
When the animations finish, `js-animation-done` class is added to the element

## Examples

```html
<caption>Animate single element</caption>
<div class="js-animate-single" data-animation-delay="0.5">Animated element</div>
```

```html
<caption>Animate sequence</caption>
<div
class="js-animate-sequence"
data-animation-interval="0.025"
data-animation-replay="true"
data-animation-selector="
.product-card > product-card__top,
.product-card > product-card__details
"
>
<div class="product-card">
<div class="product-card__top">...</div>
<div class="product-card__details">...</div>
</div>
...
</div>
```

```html
<caption>Animate complex sequence</caption>
{%- capture animation_settings -%}
[
{
"selector": ".collection-list__media",
"scale": "1.05",
"interval": "0.05",
"duration": "0.5"
},
{
"selector": ".collection-list__content",
"interval": "0.15",
"duration": "0.5"
}
]
{%- endcapture -%}
<div
class="grid-layout js-animate-sequence"
data-animation="{{  animation_settings | escape }}"
>
<div class="collection-list__item">
<div class="collection-list__media">...</div>
<div class="collection-list__content">...</div>
</div>
...
</div>
```

## Methods

| Method               | Type                            | Description                                      |
|----------------------|---------------------------------|--------------------------------------------------|
| `#updateScrollDelta` | `(): void`                      |                                                  |
| `setup`              | `(rootElement?: Element): void` | Setup animations<br /><br />Setup both single and sequence animations inside a given element<br /><br />**rootElement**: Root element inside which the animations<br />must be set-up (Default: document) |
| `setupSequence`      | `(element: Element): void`      | Set up sequence animation<br /><br />**element**: Element to animate |
| `setupSingle`        | `(element: Element): void`      | Set up single animation<br /><br />**element**: Element to animate |


# announcement-bar

Announcement bar web component.
This component displays an announcement bar with a carousel of slides.

The announcement bar shows important messages or promotions and can cycle through multiple slides.
Users can navigate the carousel manually or automatically with autoplay.
It can be configured to be dismissible and adapts to different screen sizes.

## Example

```html
<caption>Basic usage</caption>
<announcement-bar
id="announcement-bar"
class="announcement"
aria-label="Announcement Bar"
aria-live="polite"
aria-atomic="true"
static
autoplay="true"
autoplay-delay="5000"
dismissible
style="
--color: #ff5733;
--letter-spacing: 1px;
--font-size__desktop: 18px;
--font-size__mobile: 14px;
--font-weight: 600;
--text-transform: uppercase;
"
>
<div
class="
announcement__bg
announcement--divider-top
announcement--divider-bottom
section--padded
"
style="background-color: #fff;"
>
<div class="announcement__container announcement__container--carousel" tabindex="0">
<ol class="announcement__wrapper announcement__wrapper--carousel" role="list" aria-label="Announcements">
<li
 id="slide-1"
 class="announcement announcement__slides announcement__slides--carousel"
 data-slide-id="1"
 role="listitem"
 tabindex="0"
 aria-roledescription="Announcement"
 aria-label="1 of 3"
>
 <div class="announcement__message announcement__messages--1">
   <a href="#" class="announcement__link">
     <div class="announcement__text announcement__text--bold">
       <span class="announcement__icon block--1"></span>
       <span>Announcement Text 1</span>
     </div>
   </a>
 </div>
</li>
<li
 id="slide-2"
 class="announcement announcement__slides announcement__slides--carousel"
 data-slide-id="2"
 role="listitem"
 tabindex="0"
 aria-roledescription="Announcement"
 aria-label="2 of 3"
>
 <div class="announcement__message announcement__messages--2">
   <a href="#" class="announcement__link">
     <div class="announcement__text announcement__text--bold">
       <span class="announcement__icon block--2"></span>
       <span>Announcement Text 2</span>
     </div>
   </a>
 </div>
</li>
<li
 id="slide-3"
 class="announcement announcement__slides announcement__slides--carousel"
 data-slide-id="3"
 role="listitem"
 tabindex="0"
 aria-roledescription="Announcement"
 aria-label="3 of 3"
>
 <div class="announcement__message announcement__messages--3">
   <a href="#" class="announcement__link">
     <div class="announcement__text announcement__text--bold">
       <span class="announcement__icon block--3"></span>
       <span>Announcement Text 3</span>
     </div>
   </a>
 </div>
</li>
</ol>
</div>
</div>
</announcement-bar>
```

## Attributes

| Attribute        | Type      | Description                                      |
|------------------|-----------|--------------------------------------------------|
| `autoplay`       | `boolean` | Enables autoplay for the carousel.               |
| `autoplay-delay` | `string`  | Sets the delay between automatic slide transitions in milliseconds. |
| `dismissible`    | `boolean` | Makes the announcement bar dismissible by the user. |
| `static`         | `boolean` | If set, the carousel will be disabled on desktop. |

## Methods

| Method                          | Type                                             | Description                                      |
|---------------------------------|--------------------------------------------------|--------------------------------------------------|
| `#calculateSlidesWidth`         | `(): void`                                       |                                                  |
| `#createNavigation`             | `(): void`                                       |                                                  |
| `#popupListener`                | `(e: any): void`                                 |                                                  |
| `#setMaxContainerWidth`         | `(): void`                                       |                                                  |
| `#setUpDismissible`             | `(): void`                                       |                                                  |
| `#toggleClassBasedOnScreenSize` | `(): void`                                       |                                                  |
| `dismiss`                       | `(): void`                                       | Hide the announcement bar and store its state in session storage. |
| `handleIntersection`            | `(entries: any): void`                           |                                                  |
| `handleScroll`                  | `(): void`                                       |                                                  |
| `handleWindowResize`            | `(): void`                                       |                                                  |
| `moveToSlide`                   | `(slideIndex: number, behavior?: string \| undefined): void` | Move to a specific slide in the carousel.<br /><br />**slideIndex**: The index of the slide to move to.<br />**behavior**: The scroll behavior ('smooth' or 'instant'). |
| `moveToSlideById`               | `(slideId: string, behavior?: string \| undefined): void` | Move to a specific slide by its ID.<br /><br />**slideId**: The ID of the slide to move to.<br />**behavior**: The scroll behavior ('smooth' or 'instant'). |
| `observeMutations`              | `(): void`                                       |                                                  |
| `observeSlides`                 | `(): void`                                       |                                                  |
| `observeSlidesText`             | `(): void`                                       |                                                  |
| `resumeInteractions`            | `(): void`                                       | Enable user interactions with the carousel.      |
| `showNextSlide`                 | `(): void`                                       | Move to the next slide in the carousel.          |
| `showPrevSlide`                 | `(): void`                                       | Move to the previous slide in the carousel.      |
| `startAutoplay`                 | `(): void`                                       | Start the autoplay feature of the carousel.      |
| `stopAutoplay`                  | `(): void`                                       | Stop the autoplay feature of the carousel.       |
| `stopInteractions`              | `(): void`                                       | Disable user interactions with the carousel.     |

## Events

| Event                            | Type                                             | Description                                   |
|----------------------------------|--------------------------------------------------|-----------------------------------------------|
| `on:announcement-bar:dismiss`    | `CustomEvent<any>`                               | Fired when the announcement bar is dismissed. |
| `on:announcement-bar:slide:next` | `CustomEvent<{ currentSlide: number \| undefined; }>` | Fired when moving to the next slide.          |
| `on:announcement-bar:slide:prev` | `CustomEvent<{ currentSlide: number \| undefined; }>` | Fired when moving to the previous slide.      |
| `on:popup:closed`                |                                                  | Fired when a popup dialog is closed.          |
| `on:popup:opening`               |                                                  | Fired when a popup dialog is opened.          |

## CSS Custom Properties

| Property               | Description                                      |
|------------------------|--------------------------------------------------|
| `--color`              | Text color for the announcement bar.             |
| `--font-size__desktop` | Font size for the announcement text on desktop.  |
| `--font-size__mobile`  | Font size for the announcement text on mobile.   |
| `--font-weight`        | Font weight for the announcement text.           |
| `--letter-spacing`     | Letter spacing for the announcement text.        |
| `--text-transform`     | Text transform property for the announcement text. |


# back-to-top-button

Custom element that displays a "Back to Top" button.
The button appears when the user scrolls past the viewport height and scrolls the page back to the top when clicked.

## Example

```html
<caption>Basic usage</caption>
<back-to-top-button
class="back-to-top-button back-to-top-button--blue back-to-top-button--square"
aria-label="Back to top"
type="button"
role="button"
tabindex="0"
align-right
>
{% raw %}{% render 'icons-theme', icon: 'chevron', additional_classes: 'back-to-top-button__icon icon--up' %}{% endraw %}
<span class="visually-hidden">Back to top</span>
</back-to-top-button>
```

## Properties

| Property           |
|--------------------|
| `scrollToTop`      |
| `toggleVisibility` |

## Methods

| Method             | Type       | Description                                      |
|--------------------|------------|--------------------------------------------------|
| `scrollToTop`      | `(): void` | Scrolls to the top of the page smoothly or instantly. Dispatches a custom event when the button is clicked. |
| `toggleVisibility` | `(): void` | Toggles the visibility of the button based on scroll position. The button is visible when the user has scrolled past the viewport height. |

## Events

| Event                           | Type               | Description                       |
|---------------------------------|--------------------|-----------------------------------|
| `on:back-to-top-button:clicked` | `CustomEvent<any>` | Fired when the button is clicked. |


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
| `#runPostRenderFunctions`       | `(): void`                        |
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


# cart-text-input

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

| Method    | Type                      |
|-----------|---------------------------|
| `#enable` | `(e: any): Promise<void>` |


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
| `change`                     | `({ id, quantity, properties }: CartChange): Promise<any>` | Change cart line item<br /><br />**requestBody**: Cart change request body |
| `clear`                      | `(): Promise<any>`                               | Clear the shopping cart                          |
| `disableCartRecommendations` | `(): Promise<void>`                              | Disable cart recommendations                     |
| `enableCartRecommendations`  | `(intent?: string \| undefined): Promise<void>`  | Enable cart recommendations<br /><br />**intent**: Recommendations intent ("related" or "complementary") |
| `getState`                   | `(): CartStoreObject`                            | Get current cart store state                     |
| `refresh`                    | `(): Promise<any>`                               | Refresh cart                                     |
| `resetLatestAddedProduct`    | `(): Promise<void>`                              | Reset latest added product in the store          |
| `resetVariantsBeingAdded`    | `(id?: string): Promise<void>`                   | Reset variants being added<br /><br />**id**: Variant id (if not provided, all are reset) |
| `setGiftWrapping`            | `(enable?: boolean \| undefined): Promise<any>`  | Enable or disable gift wrapping<br /><br />**enable**: undefined |
| `setState`                   | `(field: string, value: string): void`           | Set store field's value<br /><br />**field**: field name to set<br />**value**: value to set |
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

A custom element that defers loading media content until it is interacted with.

## Methods

| Method        | Type                                   | Description                                      |
|---------------|----------------------------------------|--------------------------------------------------|
| `loadContent` | `(focus?: boolean \| undefined): void` | Loads the media content into the element, and optionally focuses it.<br /><br />**focus**: Whether to focus the loaded media element. |


# details-disclosure

A custom element that manages the disclosure of content within a `details` element.
It handles focus out and toggle events to control animations and visibility.

## Properties

| Property            | Type         | Default              |
|---------------------|--------------|----------------------|
| `content`           | `any \| any` | "nextElementSibling" |
| `mainDetailsToggle` | `any \| any` |                      |

## Methods

| Method       | Type       | Description                                      |
|--------------|------------|--------------------------------------------------|
| `close`      | `(): void` | Closes the disclosure by removing the `open` attribute from the `details` element<br />and setting `aria-expanded` to false on the `summary` element. |
| `onFocusOut` | `(): void` | Handles the focusout event on the `details` element.<br />Closes the disclosure if the focus moves outside the element. |
| `onToggle`   | `(): void` | Handles the toggle event on the `details` element.<br />Plays or cancels animations based on whether the `details` element is open. |


# drawer-menu

Custom element representing a drawer menu with expandable panels and focus trapping.

## Example

```html
<caption>Basic usage</caption>
<drawer-menu>
<nav class="drawer-nav drawer-nav--main">
<ul class="list-menu" role="list">
<li class="list-menu__item">
<details id="Details-menu-item-1">
 <summary class="list-menu__link">Menu Item 1</summary>
 <div id="MenuList-1" class="drawer-nav__panel">
   <ul class="list-menu" role="list">
     <li class="list-menu__item">
       <details id="Details-submenu-item-1">
         <summary class="list-menu__link">Submenu Item 1</summary>
         <div id="ChildMenuList-1" class="drawer-nav__panel">
           <ul class="list-menu" role="list">
             <li class="list-menu__item">
               <a href="#" class="list-menu__link">Grandchild Item 1</a>
             </li>
           </ul>
         </div>
       </details>
     </li>
   </ul>
 </div>
</details>
</li>
<li class="list-menu__item">
<a href="#" class="list-menu__link">Menu Item 2</a>
</li>
</ul>
</nav>
</drawer-menu>
```

## Methods

| Method                       | Type                                             | Description                                      |
|------------------------------|--------------------------------------------------|--------------------------------------------------|
| `bindEvents`                 | `(): void`                                       | Binds click event listeners to summary and button elements within the drawer menu. |
| `closeAllOpenPanels`         | `(): void`                                       | Closes all currently open panels.                |
| `closeSubmenu`               | `(detailsElement: HTMLElement, animate?: boolean \| undefined): void` | Closes a submenu panel and optionally animates the closing.<br /><br />**detailsElement**: The details element to close.<br />**animate**: Whether to animate the closing. |
| `disableBannerHeightControl` | `(): void`                                       | Disables control of the banner height by disconnecting the observer. |
| `enableBannerHeightControl`  | `(banner: HTMLElement): void`                    | Enables control of the banner height for a given banner element.<br /><br />**banner**: The banner element to control the height of. |
| `onCloseButtonClick`         | `(event: Event): void`                           | Handles click events on close buttons to close the associated panels.<br /><br />**event**: The click event. |
| `onSummaryClick`             | `(event: Event): void`                           | Handles click events on summary elements to toggle panels.<br /><br />**event**: The click event. |
| `openMenuPanelById`          | `(id: string, animate?: boolean \| undefined, focus?: boolean \| undefined): void` | Opens a menu panel by its ID, optionally animating and focusing it.<br /><br />**id**: The ID of the panel to open.<br />**animate**: Whether to animate the opening.<br />**focus**: Whether to focus the panel. |
| `openPanel`                  | `(detailsElement: HTMLElement, focus?: boolean \| undefined): string` | Opens a panel and optionally focuses it.<br /><br />**detailsElement**: The details element to open.<br />**focus**: Whether to focus the panel. |
| `setCurrentPanelId`          | `(): void`                                       | Sets the ID of the currently open panel, if any. |


# dynamic-button

Dynamic button component

Used as the container with a placeholder for dynamic Shopify buttons

## Example

```html
<caption>Basic usage</caption>
<dynamic-button class="dynamic-button">
<div class="dynamic-button__placeholder skeleton-button">
<span
class="skeleton-text skeleton-text--inverse skeleton-text--small skeleton-text--inline skeleton-text--1/2"
></span>
</div>
{{ form | payment_button }}
</dynamic-button>
```


# dynamic-product-search

Dynamic product search

A custom web component for handling dynamic product searches,
including pagination, filtering, and URL updates.

## Example

```html
<dynamic-product-search
  data-section="products"
  data-url="https://example.com/api/products"
  data-update-url="true"
  data-page-title="Product Search"
  data-quick-shop-dynamic-checkout="true"
></dynamic-product-search>
```

## Attributes

| Attribute                          | Type     | Default | Description                                      |
|------------------------------------|----------|---------|--------------------------------------------------|
| `data-page-title`                  | `string` |         | The title of the page to set when the URL is updated. |
| `data-quick-shop-dynamic-checkout` | `string` | "false" | Enables or disables the dynamic checkout button. |
| `data-section`                     | `string` |         | The identifier for the product section.          |
| `data-update-url`                  | `string` | "true"  | Determines whether the URL should be updated when the collection changes. |
| `data-url`                         | `string` |         | The base URL for the product search API.         |

## Methods

| Method             | Type                                             | Description                                      |
|--------------------|--------------------------------------------------|--------------------------------------------------|
| `renderCollection` | `(params: { query: string; updateURL: boolean; scrollUp: boolean; }): void` | Renders a collection of products based on the provided parameters.<br />Updates the URL, scrolls the page, and manages the loading state.<br /><br />**params.query**: The query string to filter products. |
| `renderError`      | `(e?: string \| undefined): void`                | Renders an error message within the component.<br /><br />**e**: The error message to display. |
| `scrollUp`         | `(): void`                                       | Scrolls the window up to the top of the section. |
| `updateLoading`    | `(isLoading?: boolean \| undefined): void`       | Updates the loading state of the component.<br /><br />**isLoading**: Indicates whether the component is in a loading state. |
| `updateURL`        | `(query: string, title?: string): void`          | Updates the URL in the browser's history.<br /><br />**query**: The query string to append to the URL.<br />**title**: The title of the page. |

## Events

| Event                               | Type               | Description                                      |
|-------------------------------------|--------------------|--------------------------------------------------|
| `on:dynamic-product-search:failed`  | `CustomEvent<any>` | Dispatched when the product search fails to load. |
| `on:dynamic-product-search:loaded`  | `CustomEvent<any>` | Dispatched when the product search has finished loading. |
| `on:dynamic-product-search:loading` | `CustomEvent<any>` | Dispatched when the product search starts loading. |


# filters-dialog

A custom element that extends `ModalDialog` to provide a modal dialog with filters.
It initializes and destroys the dialog based on the viewport width and media query changes.

## Attributes

| Attribute                       | Type      | Description                |
|---------------------------------|-----------|----------------------------|
| `data-disable-modal-on-desktop` | `boolean` | Disables modal on desktop. |

## Methods

| Method    | Type       | Description                                      |
|-----------|------------|--------------------------------------------------|
| `destroy` | `(): void` | Destroys the dialog by removing ARIA attributes and CSS classes.<br />Calls the parent class's `destroy` method. |
| `init`    | `(): void` | Initializes the dialog by setting ARIA attributes and CSS classes.<br />Calls the parent class's `init` method. |


# gift-card-recipient

A custom element that manages the activation of a fieldset based on a checkbox.
When the checkbox is checked, it enables and reveals the associated fields.
When unchecked, it disables and hides them.

## Properties

| Property   | Type                  |
|------------|-----------------------|
| `checkbox` | `any \| any`          |
| `fields`   | `NodeListOf<Element>` |
| `fieldset` | `any \| any`          |

## Methods

| Method             | Type       | Description                                      |
|--------------------|------------|--------------------------------------------------|
| `activateFieldset` | `(): void` | Activates or deactivates the fieldset based on the checkbox's checked state.<br />Enables and reveals the fields if the checkbox is checked,<br />otherwise, disables and hides them. |


# header-container

A custom element that manages the visibility and sticky behavior of a header
based on scroll events. The header can be configured to stick to the top of
the viewport and hide or show based on scroll direction.

## Attributes

| Attribute | Type      | Description                          |
|-----------|-----------|--------------------------------------|
| `sticky`  | `boolean` | Whether the header should be sticky. |


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


# image-compare

Custom element for comparing images with a sliding effect.
Allows users to adjust the exposure level of an image via a slider.
Also includes an intersection observer to animate the slider when it enters the viewport.

## Example

```html
<caption>Basic usage</caption>
<image-compare
style="
--exposure: 50%;
--thumb-border-color: #ff0000;
--divider-color: #ff0000;
--thumb-background-color: #ffffff;
--image-background-color: #000000;
"
data-start-point="50"
data-grow-thumb="true"
>

<div class="image-compare__media-item image-compare__media-item--before">
<div class="o-ratio o-ratio--16by9 o-ratio--16by9@mob">
<div class="o-ratio__content">
<img src="image1.jpg" alt="Before Image" class="image-compare__image" />
<div class="image-compare__image-background"></div>
</div>
</div>
</div>

<div class="image-compare__media-item image-compare__media-item--after">
<div class="o-ratio o-ratio--16by9 o-ratio--16by9@mob">
<div class="o-ratio__content">
<img src="image2.jpg" alt="After Image" class="image-compare__image" />
<div class="image-compare__image-background"></div>
</div>
</div>
</div>

<label>
<span class="u-hidden-visually">Control how much of each overlapping image is shown</span>
<input type="range" value="50" min="0" max="100" step="0.1">
</label>
</image-compare>
```

## Attributes

| Attribute          | Type      | Description                                 |
|--------------------|-----------|---------------------------------------------|
| `data-grow-thumb`  | `boolean` | If true, the thumb will grow when hovered.  |
| `data-start-point` | `string`  | The initial exposure value as a percentage. |

## CSS Custom Properties

| Property                   | Description                              |
|----------------------------|------------------------------------------|
| `--divider-color`          | The color of the divider line.           |
| `--exposure`               | The current exposure level of the image. |
| `--image-background-color` | The background color of the images.      |
| `--thumb-background-color` | The background color of the thumb.       |
| `--thumb-border-color`     | The border color of the thumb.           |


# image-skeleton

Image Skeleton
A custom web component that provides a skeleton loader for images to enhance loading performance.
This component displays a placeholder while an image is loading, and only reveals the image once it has fully loaded.

## Example

```html
<caption>Basic usage</caption>
<image-skeleton minimum-reveal-delay="250">
<span class="visually-hidden">Image alt text</span>
<svg
id="visual"
viewBox="0 0 400 300"
width="400"
height="300"
xmlns="http://www.w3.org/2000/svg"
>
<rect x="0" y="0" width="400" height="300"></rect>
</svg>
</image-skeleton>
```

## Attributes

| Attribute              | Type      | Description                                     |
|------------------------|-----------|-------------------------------------------------|
| `loaded`               | `boolean` | If true, the image has already been loaded.     |
| `minimum-reveal-delay` | `number`  | The minimum delay before the image is revealed. |

## Methods

| Method         | Type       | Description                                      |
|----------------|------------|--------------------------------------------------|
| `init`         | `(): void` | Initializes the skeleton loader by checking the associated image element.<br />Sets up an event listener to reveal the image after it has fully loaded. |
| `markAsLoaded` | `(): void` | Marks the skeleton loader as loaded and hides it.<br />Sets the 'loaded' and 'aria-hidden' attributes. |


# interactive-map

A custom HTML element that displays an interactive Google Map with specified
settings, including custom styles and a pin based on provided attributes.

## Attributes

| Attribute       | Type     | Description                                      |
|-----------------|----------|--------------------------------------------------|
| `api-key`       | `string` | The API key for accessing Google Maps services.  |
| `map-address`   | `string` | The address to be geocoded and marked on the map. |
| `map-pin-style` | `string` | The style to be applied to the map pin.          |
| `map-style`     | `string` | The style to be applied to the map.              |


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


# lazy-video

A custom HTML element that lazily loads and plays video content
when it becomes visible in the viewport.


# localize-details-disclosure

A custom element that extends DetailsDisclosure to handle localization
details disclosure with form interaction.


# maps-with-details

Custom HTML element that synchronizes a set of `<details>` elements with associated map media elements.
When a specific `<details>` element is opened, it triggers the display of the corresponding map media.


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
{% raw %}{%- render 'icons-theme', icon: 'chevron, additional_classes: 'icon--left' -%}{% endraw %}
</button>
<button
class="
media-gallery__arrow
media-gallery__arrow--next
js-carousel-next
"
>
{% raw %}{%- render 'icons-theme', icon: 'chevron -%}{% endraw %}
</button>

<!-- Virtual slides -->
<div class="js-slides u-hidden-visually">
...
</div>
</media-carousel>
```

## Attributes

| Attribute             | Description                                      |
|-----------------------|--------------------------------------------------|
| `data-auto-height`    | Enable auto height                               |
| `data-autoplay`       | Enable autoplay with provided delay value        |
| `data-breakpoint-max` | Only enable from the breakpoint ('phab', 'tab', 'desk') |
| `data-breakpoint-min` | Only enable up to the breakpoint ('phab', 'tab', 'desk') |
| `data-fade`           | Enable fade effect                               |
| `data-initial-slide`  | Initial slide                                    |
| `data-loop`           | Enable loop                                      |
| `data-navigation`     | Enable navigation                                |
| `data-pagination`     | Enable bullets pagination                        |
| `data-space-between`  | Space between slides (Default: 30px)             |
| `data-speed`          | Animation speed (Default: 200ms)                 |
| `data-virtual`        | Enable virtual slides (element with the class '.js-slides'<br />has to be present inside the container) |

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

| Event                                    | Type     | Description                         |
|------------------------------------------|----------|-------------------------------------|
| `on:media-carousel:before-slide-change`  | `Object` | Before media carousel slide change  |
| `on:media-carousel:init`                 | `Object` | Media carousel initialized          |
| `on:media-carousel:slide-change`         | `Object` | Media carousel slide changed        |
| `on:media-carousel:slide-transition-end` | `Object` | Media carousel slide transition end |


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
{% raw %}{% render 'icons-theme', icon: 'close' %}{% endraw %}
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
{% raw %}{% render 'icons-theme', icon: 'close' %}{% endraw %}
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

Custom HTML element for a predictive search component, providing real-time search suggestions as the user types.
This component handles search input, results display, keyboard navigation, and loading state management.

## Example

```html
<caption>Main search</caption>
<predictive-search
dropdown
type="main"
search-url="/search"
>
<script src="predictive-search.js" type="module"></script>
<search-form add-recent-search-on-load>
<form
is="search-form"
action="/search"
method="get"
class="search-page__form js-search-form js-animate-single"
data-animation-displacement="0"
data-animation-delay="0.1"
role="search"
>
<div class="search__form-input-wrapper">
<input
 id="main-search"
 type="search"
 name="q"
 value=""
 placeholder="Search"
 class="search-page__form-input"
 aria-label="Search"
 role="combobox"
 aria-expanded="false"
 aria-owns="main-predictive-search-results"
 aria-controls="main-predictive-search-results"
 aria-haspopup="listbox"
 aria-autocomplete="list"
 autocorrect="off"
 autocomplete="off"
 autocapitalize="off"
 spellcheck="false"
>
<button
 type="submit"
 class="search-page__form-submit"
 aria-label="Submit"
>
 <svg class="icon" aria-hidden="true">
   <use href="#search-icon"></use>
 </svg>
</button>
</div>
<predictive-search-results tabindex="-1" hidden></predictive-search-results>
</form>
</search-form>
</predictive-search>
```

## Attributes

| Attribute    | Type      | Description                                      |
|--------------|-----------|--------------------------------------------------|
| `dropdown`   | `boolean` | If present, the component operates as a dropdown, handling focus and blur events differently. |
| `open`       | `boolean` | Indicates whether the search results panel is open or not. |
| `results`    | `boolean` | If set to 'true', indicates that there are search results available. |
| `search-url` | `string`  | The URL used to fetch search suggestions.        |

## Properties

| Property     | Attribute | Type      | Description                                      |
|--------------|-----------|-----------|--------------------------------------------------|
| `isDropdown` |           | `boolean` |                                                  |
| `type`       | `type`    | `string`  | The type of search, typically used to distinguish between different layouts (e.g., 'sidebar'). |

## Methods

| Method             | Type                                  | Description                                      |
|--------------------|---------------------------------------|--------------------------------------------------|
| `close`            | `(): void`                            | Closes the predictive search results panel.      |
| `getQuery`         | `(): string`                          | Retrieves the current search query from the input field. |
| `getSearchResults` | `(searchTerm: string): Promise<void>` | Fetches search results from the server based on the current search term.<br /><br />**searchTerm**: The current search term. |
| `open`             | `(): void`                            | Opens the predictive search results panel.       |
| `selectOption`     | `(): void`                            | Selects the currently highlighted search option. |
| `switchOption`     | `(direction: string): void`           | Switches between search options using the arrow keys.<br /><br />**direction**: The direction to move ('up' or 'down'). |


# price-range

Custom HTML element for a price range slider component, allowing users to select a range of prices.
This component synchronizes two range sliders with corresponding number inputs.

## Example

```html
<caption>Advanced usage with dynamic values</caption>
<price-range class="price-range">
<div class="collection-sidebar__filter-price">
<div class="collection-sidebar__filter-price__item collection-sidebar__filter-price__item--from">
<span class="collection-sidebar__filter-price__currency">$</span>
<input
name="min_price"
id="Filter-Price-min"
class="collection-sidebar__filter-price__input price-range__number"
value="250"
type="number"
inputmode="numeric"
placeholder="0"
min="0"
max="1000"
>
<label for="Filter-Price-min" class="collection-sidebar__filter-price__label">From</label>
</div>
<div class="collection-sidebar__filter-price__item collection-sidebar__filter-price__item--separator">-</div>
<div class="collection-sidebar__filter-price__item collection-sidebar__filter-price__item--to">
<span class="collection-sidebar__filter-price__currency">$</span>
<input
name="max_price"
id="Filter-Price-max"
class="collection-sidebar__filter-price__input price-range__number"
value="750"
type="number"
inputmode="numeric"
placeholder="1000"
min="0"
max="1000"
>
<label for="Filter-Price-max" class="collection-sidebar__filter-price__label">To</label>
</div>
</div>
<div class="price-range__group">
<div class="price-range__track">
<label class="u-hidden-visually" for="Filter-Price-Track-1">Price range minimum</label>
<input
class="price-range__input"
value="250"
min="0"
max="1000"
type="range"
tabindex="-1"
id="Filter-Price-Track-1"
>
<label class="u-hidden-visually" for="Filter-Price-Track-2">Price range maximum</label>
<input
class="price-range__input"
value="750"
min="0"
max="1000"
type="range"
tabindex="-1"
id="Filter-Price-Track-2"
>
</div>
</div>
</price-range>
```


# product-card-spinner

Custom HTML element for managing the loading spinner logic of a product image within a product card.
This component observes changes to the `src` attribute of an image element and displays a loading spinner while the image is loading.

## Properties

| Property       | Type     | Default   |
|----------------|----------|-----------|
| `loadingClass` | `string` | "loading" |


# product-card-swatches

Custom HTML element representing a product card with swatches.
This element allows users to select different product variants by clicking on swatches,
which updates the product image and variant link.

## Properties

| Property      | Type                  |
|---------------|-----------------------|
| `hoverImage`  | `any \| any`          |
| `image`       | `any \| any`          |
| `product`     | `any \| any`          |
| `productLink` | `any \| any`          |
| `triggers`    | `NodeListOf<Element>` |

## Methods

| Method                   | Type                             | Description                                      |
|--------------------------|----------------------------------|--------------------------------------------------|
| `updateCardImage`        | `(swatch: HTMLElement): boolean` | Updates the product card image and product variant link based on the selected swatch.<br /><br />**swatch**: The swatch element that was clicked. |
| `updateQuickShopVariant` | `(swatch: HTMLElement): void`    | Updates the quick shop variant with the selected swatch's variant ID.<br /><br />**swatch**: The swatch element that was clicked. |


# product-card-mini

A custom element that represents a mini product card.
Handles rendering of product details, image updates, and quick shop functionality.

## Example

```html
<caption>Basic usage</caption>
<product-card-mini
rendered
data-product-id="{{ current_product.id }}"
class="{{ product_card_classes }}"
image-container-ratio="{{ container_ratio }}"
image-fit
section-id="{{ section_id }}"
quick-shop-trigger="{{ quick_shop_trigger }}"
move-quick-shop
>
<a product-card-link href="{{ link }}" class="product-card__link">
<span class="visually-hidden">{{ title }}</span>
</a>
<div class="product-card__top">
<div class="o-ratio o-ratio--{{ container_ratio }}"
style="padding-bottom:{{ image_container_bottom_padding }}">
<div class="o-ratio__content">
<a product-card-link href="{{ link }}" tabindex="-1">
 <div class="product-card__media product-card__media--hover-image">
   <product-card-secondary-image-placeholder
     class="product-card__img-hover hover-enabled">
     {% raw %}{% render 'image', image: secondary_image, additional_classes: 'product-card__img-hover hover-enabled' %}{% endraw %}
   </product-card-secondary-image-placeholder>
   {% raw %}{% render 'image', image: image, additional_classes: 'product-card__img js-product-card-image' %}{% endraw %}
 </div>
</a>
</div>
</div>
</div>
<div class="product-card__details">
<h3 class="product-card__title">
<product-card-title>{{ current_product.title }}</product-card-title>
</h3>
<product-card-price class="product-card__price">
{% raw %}{% render 'product-price', product: current_product %}{% endraw %}
</product-card-price>
<product-card-button class="product-card-btn">
<button type="button" class="link" disabled="disabled">{{ 'products.product.sold_out' | t }}</button>
</product-card-button>
</div>
</product-card-mini>
```

## Attributes

| Attribute               | Type      | Description                                      |
|-------------------------|-----------|--------------------------------------------------|
| `image-container-ratio` | `string`  | The ratio of the image container (e.g., "natural"). |
| `image-fit`             | `boolean` | Determines if the image should fit within its container. |
| `image-hover`           | `boolean` | Determines the hover effect for the image (e.g., "zoom"). |
| `move-quick-shop`       | `boolean` | Indicates if the quick shop should be moved to a different container. |
| `quick-shop-trigger`    | `string`  | Specifies the type of quick shop trigger (e.g., "button"). |
| `rendered`              | `boolean` | Indicates if the product card has been rendered. |

## Properties

| Property  | Attribute | Type     | Description                                      |
|-----------|-----------|----------|--------------------------------------------------|
| `id`      | `id`      | `string` | Sets the ID of the product card and updates the quick shop ID if present. |
| `product` |           |          | Sets the product data and triggers the rendering process if necessary. |

## Methods

| Method           | Type                                             | Description                                      |
|------------------|--------------------------------------------------|--------------------------------------------------|
| `renderImage`    | `(url: string, width: number, height: number, classes?: string \| undefined, alt?: string \| undefined, sizes?: string \| undefined, srcsetWidths?: number[] \| undefined): HTMLImageElement\|null` | Renders an image element with the provided URL, width, and height,<br />and optional classes, alt text, and sizes. The image is created with<br />a srcset attribute for responsive images.<br /><br />**url**: The URL of the image.<br />**width**: The width of the image.<br />**height**: The height of the image.<br />**classes**: The classes to apply to the image element.<br />**alt**: The alt text for the image.<br />**sizes**: The sizes attribute for the image.<br />**srcsetWidths**: The widths for the srcset attribute. |
| `updateImage`    | `(url: string, width: number, height: number, alt?: string \| undefined, srcsetWidths?: number[] \| undefined): void` | Updates the image element with the provided URL, width, height, and alt text.<br />It also generates a srcset attribute for responsive images based on the provided srcsetWidths.<br /><br />**url**: The URL of the image.<br />**width**: The width of the image.<br />**height**: The height of the image.<br />**alt**: The alt text of the image.<br />**srcsetWidths**: An array of widths for the srcset. |
| `updateSkeleton` | `(): void`                                       | Updates the skeleton element associated with the image.<br />It checks if the image has a sibling element with the tag name 'image-skeleton' and updates its attributes accordingly. |


# product-card

Custom HTML element representing a product card.
This element extends the ProductCardMini class and provides additional functionality specific to the product card.

## Example

```html
<caption>Basic usage</caption>
<product-card
rendered
data-product-id="12345"
class="product-card--custom"
image-container-ratio="1:1"
image-hover="zoom"
image-fit
section-id="featured-products"
quick-shop-trigger="icon"
move-quick-shop
>
<div class="product-card-top">
<a product-card-link href="/product/12345" class="product-card__link">
<div class="product-card__media product-card__media--hover-zoom">
<img src="/path/to/image.jpg" alt="Product Image" class="product-card__img" />
</div>
</a>
</div>
<div class="product-card__details">
<a product-card-link href="/product/12345" class="product-card__link">
<h3 class="product-card__title">Product Title</h3>
</a>
<div class="product-card__details__hover">
<product-card-price class="price">$29.99</product-card-price>
<product-card-reviews class="review-wrapper">
<div class="rating" role="img" aria-label="Rated 4.5 out of 5 stars">
 <span class="rating-star" style="--rating: 4.5;"></span>
</div>
<p class="rating-count">(150 reviews)</p>
</product-card-reviews>
</div>
</div>
</product-card>
```

## Attributes

| Attribute               | Type      | Description                                      |
|-------------------------|-----------|--------------------------------------------------|
| `image-container-ratio` | `string`  | The ratio of the image container (e.g., "natural"). |
| `image-fit`             | `boolean` | Determines if the image should fit within its container. |
| `image-hover`           | `boolean` | Determines the hover effect for the image (e.g., "zoom"). |
| `move-quick-shop`       | `boolean` | Indicates if the quick shop should be moved to a different container. |
| `quick-shop-trigger`    | `string`  | Specifies the type of quick shop trigger (e.g., "button"). |
| `rendered`              | `boolean` | Indicates if the product card has been rendered. |

## Properties

| Property  | Attribute | Type     | Description                                      |
|-----------|-----------|----------|--------------------------------------------------|
| `id`      | `id`      | `string` | Sets the ID of the product card and updates the quick shop ID if present. |
| `product` |           |          | Sets the product data and updates the current variant URL and swatches listeners if necessary. |

## Methods

| Method           | Type                                             | Description                                      |
|------------------|--------------------------------------------------|--------------------------------------------------|
| `renderImage`    | `(url: string, width: number, height: number, classes?: string \| undefined, alt?: string \| undefined, sizes?: string \| undefined, srcsetWidths?: number[] \| undefined): HTMLImageElement\|null` | Renders an image element with the provided URL, width, and height,<br />and optional classes, alt text, and sizes. The image is created with<br />a srcset attribute for responsive images.<br /><br />**url**: The URL of the image.<br />**width**: The width of the image.<br />**height**: The height of the image.<br />**classes**: The classes to apply to the image element.<br />**alt**: The alt text for the image.<br />**sizes**: The sizes attribute for the image.<br />**srcsetWidths**: The widths for the srcset attribute. |
| `setVariant`     | `(e: Event): void`                               | Updates the product variant based on the selected variant ID.<br /><br />**e**: The event object triggered by the variant selection. |
| `updateImage`    | `(url: string, width: number, height: number, alt?: string \| undefined, srcsetWidths?: number[] \| undefined): void` | Updates the image element with the provided URL, width, height, and alt text.<br />It also generates a srcset attribute for responsive images based on the provided srcsetWidths.<br /><br />**url**: The URL of the image.<br />**width**: The width of the image.<br />**height**: The height of the image.<br />**alt**: The alt text of the image.<br />**srcsetWidths**: An array of widths for the srcset. |
| `updateSkeleton` | `(): void`                                       | Updates the skeleton element associated with the image.<br />It checks if the image has a sibling element with the tag name 'image-skeleton' and updates its attributes accordingly. |


# product-form

Interactive product form

## Example

```html
<caption>Basic usage</caption>
<product-form
{% unless settings.cart_type == 'page' %}
notify-on-add
{% else %}
redirect-on-add="{{ routes.cart_url }}"
{% endunless %}
>
{% raw %}{% form 'product', product, class: 'product-form', id: form_id %}
...
{% endform %}{% endraw %}
</product-form>
```

## Attributes

| Attribute         | Description                                |
|-------------------|--------------------------------------------|
| `notify-on-add`   | Trigger cart drawer or notification on add |
| `redirect-on-add` | Redirect to given page on add              |

## Methods

| Method        | Type                        | Description                         |
|---------------|-----------------------------|-------------------------------------|
| `removeError` | `(): void`                  | Remove error element                |
| `submit`      | `(e: Event): Promise<void>` | Submit form<br /><br />**e**: Event |


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


# product-model

A custom element that extends DeferredMedia to load and set up 3D model viewers
for product pages. It integrates Shopify's Model Viewer UI for enhanced interaction
with 3D models.

## Example

```html
<caption>Basic usage</caption>
<product-model
class="
media-gallery__item
media-gallery__item--model
deferred-media
"
data-slide-id="{{ forloop.index0 }}"
data-media-id="{{ media.id }}"
>
<media-poster>
{{ media.preview_image | image_url: width: 1946 | image_tag:
loading: lazy,
sizes: sizes,
widths: '246, 493, 600, 713, 823, 990, 1100, 1206, 1346, 1426, 1646, 1946'
}}
</media-poster>
<template>
{{ media | media_tag: image_size: "2048x", toggleable: true }}
</template>
</product-model>
```

## Methods

| Method               | Type                    | Description                                      |
|----------------------|-------------------------|--------------------------------------------------|
| `loadContent`        | `(): void`              | Loads the necessary content and initializes the Shopify Model Viewer UI.<br />Overrides the `loadContent` method from DeferredMedia. |
| `setupModelViewerUI` | `(errors: Array): void` | Sets up the Shopify Model Viewer UI by attaching it to the `model-viewer` element.<br />Dispatches a custom event when the model is loaded.<br /><br />**errors**: An array of errors that may occur during setup. |

## Events

| Event                     | Type               | Description                     |
|---------------------------|--------------------|---------------------------------|
| `on:product-model:loaded` | `CustomEvent<any>` | Fired when the model is loaded. |


# product-recommendations

A custom element that loads product recommendations from a URL and updates the DOM with the fetched content.

## Example

```html
<caption>Basic usage</caption>
<product-recommendations
id="recommended-products"
data-url="/api/products/recommendations"
data-quick-shop-dynamic-checkout
>
</product-recommendations>
```

## Attributes

| Attribute                          | Type      | Description                                      |
|------------------------------------|-----------|--------------------------------------------------|
| `data-quick-shop-dynamic-checkout` | `boolean` | Determines if the quick shop dynamic checkout is enabled. |
| `data-url`                         | `string`  | The URL used to fetch product recommendations.   |
| `id`                               | `string`  | The unique identifier for the element.           |

## Properties

| Property      | Type     | Default |
|---------------|----------|---------|
| `fetch_delay` | `number` | 0       |


# product-single

A custom HTML element representing a single product page with media gallery and variant management.

This element handles the display and update of media in a product gallery based on the selected variant.

## Properties

| Property  | Description                                      |
|-----------|--------------------------------------------------|
| `variant` | Sets the variant property and updates the media gallery accordingly. |

## Methods

| Method        | Type       | Description                                      |
|---------------|------------|--------------------------------------------------|
| `updateMedia` | `(): void` | Updates the media gallery to show the featured media of the current variant. |


# quantity-input

Custom HTML element for managing quantity input with increment and decrement buttons.
This component handles user interaction with the quantity input, including validation and updates.

## Example

```html
<caption>Basic usage</caption>
<quantity-input>
<button minus type="button" aria-label="Reduce quantity">
<span aria-hidden="true">&minus;</span>
</button>
<input
id="quantity-input"
type="number"
value="1"
min="1"
step="1"
name="quantity"
autocomplete="off"
>
<button plus type="button" aria-label="Increase quantity">
<span aria-hidden="true">+</span>
</button>
</quantity-input>
```

## Attributes

| Attribute | Type     | Description               |
|-----------|----------|---------------------------|
| `max`     | `number` | The maximum value allowed |
| `min`     | `number` | The minimum value allowed |
| `step`    | `number` | The step value            |

## Properties

| Property | Type     | Description                    |
|----------|----------|--------------------------------|
| `value`  | `number` | Sets the quantity input value. |

## Methods

| Method     | Type               | Description                                      |
|------------|--------------------|--------------------------------------------------|
| `add`      | `(): void`         | Increases the quantity value by the defined step, but not above the maximum value. |
| `subtract` | `(): void`         | Decreases the quantity value by the defined step, but not below the minimum value. |
| `validate` | `(e: Event): void` | Validates the quantity input value against the minimum and maximum constraints.<br /><br />**e**: The input change event. |

## Events

| Event    | Type          | Description                             |
|----------|---------------|-----------------------------------------|
| `update` | `CustomEvent` | Dispatched when the quantity is updated |


# quick-shop

A custom HTML element that represents a Quick Shop modal dialog, extending the ModalDialog class.

This element handles displaying a quick shop modal with product details, including variant updates and media handling.
It also manages modal opening/closing events and fetches quick shop content based on proximity or user interaction.

## Example

```html
<caption>Basic usage</caption>
<quick-shop
data-product-url="https://example.com/product-url"
image-container-ratio="16:9"
image-sizes="(min-width: 600px) 50vw, 100vw"
image-fit
load-on="click"
placeholder
card-id="product-card-123"
aria-labelledby="quick-shop-title"
aria-hidden="true"
>
<!-- Modal content goes here -->
</quick-shop>
```

## Attributes

| Attribute               | Type      | Description                                      |
|-------------------------|-----------|--------------------------------------------------|
| `aria-hidden`           | `boolean` | Indicates whether the component is hidden from accessibility tools. |
| `aria-labelledby`       | `string`  | The ID of the element used to label the component for accessibility. |
| `card-id`               | `string`  | The ID associated with the product card.         |
| `data-product-url`      | `string`  | The URL of the product to display.               |
| `image-container-ratio` | `string`  | The aspect ratio of the image container.         |
| `image-fit`             | `boolean` | Whether to fit the image to the container.       |
| `image-sizes`           | `string`  | The sizes attribute for responsive images.       |
| `notify-on-add`         | `boolean` | Whether to notify on adding the product to the cart. |
| `placeholder`           | `boolean` | Whether to display a placeholder image if no product image is available. |

## Properties

| Property    | Type               | Description                                      |
|-------------|--------------------|--------------------------------------------------|
| `variantId` | `string \| number` | Sets the current variant ID and updates the variant. |

## Methods

| Method  | Type         | Description                                      |
|---------|--------------|--------------------------------------------------|
| `close` | `(): string` | Closes the quick shop modal and resolves with a 'Closed' message. |

## Events

| Event                   | Type               | Description                                      |
|-------------------------|--------------------|--------------------------------------------------|
| `on:quick-shop:failed`  | `CustomEvent<any>` | Fired when the quick shop content fails to load. |
| `on:quick-shop:loaded`  | `CustomEvent<any>` | Fired when the quick shop content has been successfully loaded. |
| `on:quick-shop:loading` | `CustomEvent<any>` | Fired when the quick shop content starts loading. |


# recent-searches

A custom web component that displays a list of recent search queries.

The component retrieves recent searches from localStorage and updates its content accordingly.

## Example

```html
<caption>Basic usage</caption>
<recent-searches class="search__nav" hidden>
<h4 class="search__nav-title">
{{ 'general.search.recent_searches.title' | t }}
</h4>
<ul class="search__nav-items o-list-bare"></ul>
</recent-searches>
```

## Attributes

| Attribute | Type     | Description                                  |
|-----------|----------|----------------------------------------------|
| `hidden`  | `string` | Indicates if the component should be hidden. |


# scroll-to-target

A custom HTML element that smooth scrolls to a target element when a link is clicked.

## Example

```html
<scroll-to-target>
  <a href="#targetElementId">Scroll to Target</a>
</scroll-to-target>
```

## Attributes

| Attribute | Type     | Description                                |
|-----------|----------|--------------------------------------------|
| `href`    | `string` | The ID of the target element to scroll to. |


# scrolling-marquee

A custom element that controls a scrolling marquee effect for its children.

## Example

```html
<caption>Basic usage</caption>
<scrolling-marquee
id="scrolling-marquee"
marquee-speed="5"
role="marquee"
aria-label="Scrolling Text"
tabindex="0"
>
<div class="container container--full container--p-0">
<div class="scrolling-text__bg u-bg-overlay scrolling-text__pattern--fill">
<div class="scrolling-text__bg-overlay section--padded">
<div class="scrolling-text__pattern">
 <div class="marquee">
   <ul class="marquee__content marquee--reverse marquee--pause" role="list">
     <li class="marquee-text" role="listitem">
       <a href="https://example.com">
         <div class="scrolling__text scrolling__text--bold scrolling__text--f-caps">
           <span>Example Text 1</span>
         </div>
       </a>
     </li>
     <li class="marquee-icon" role="listitem">
       <a href="https://example.com">
         <div class="scrolling__icon scrolling__icon--custom">
           <!-- Icon SVG or code -->
         </div>
       </a>
     </li>
   </ul>
 </div>
</div>
</div>
</div>
</div>
</scrolling-marquee>
```

## Attributes

| Attribute       | Type     | Description                           |
|-----------------|----------|---------------------------------------|
| `marquee-speed` | `number` | The speed at which the marquee moves. |

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

| Method            | Type       | Description                                      |
|-------------------|------------|--------------------------------------------------|
| `observeMarquee`  | `(): void` | Observes the marquee container for changes.      |
| `setMarqueeSpeed` | `(): void` | Sets the animation duration for each marquee element based on the marquee speed. |


# search-form

A custom HTML element that manages and stores recent search queries.

This element retrieves and stores recent searches in `localStorage` and updates all instances of the `recent-searches` component when a new search is added.

## Example

```html
<caption>Basic usage</caption>
<search-form add-recent-search-on-load>
<form
action="{{ routes.search_url }}"
method="get"
class="search-page__form js-search-form"
role="search"
>
<div class="search__form-input-wrapper">
<input
id="main-search"
type="search"
name="q"
value="{{ search.terms | escape }}"
placeholder="{{ 'general.search.placeholder' | t }}"
class="search-page__form-input"
aria-label="{{ 'general.search.placeholder' | t }}"
>
<button type="submit" class="search-page__form-submit" aria-label="{{ 'general.search.submit' | t }}">
{% raw %}{% render 'icons-theme', icon: 'search' %}{% endraw %}
</button>
</div>
</form>
</search-form>
```

## Attributes

| Attribute                   | Type      | Description                                      |
|-----------------------------|-----------|--------------------------------------------------|
| `add-recent-search-on-load` | `boolean` | If present, adds the current form state to the recent searches list when the element is connected to the DOM. |

## Properties

| Property | Type         |
|----------|--------------|
| `form`   | `any \| any` |

## Methods

| Method                         | Type       | Description                                      |
|--------------------------------|------------|--------------------------------------------------|
| `addFormStateToRecentSearches` | `(): void` | Adds the current form state to the recent searches list by constructing a search URI and invoking `addRecentSearch`.<br /><br />This method collects form data, constructs a URL including the query parameters, and adds the search to the recent searches list. |


# search-modal

A custom HTML element that extends `ModalDialog` to provide a searchable modal interface.

This element integrates with the ModalDialog class and manages a predictive search component within the modal.
It handles closing the predictive search and clearing the search input when the modal is closed.

## Example

```html
<caption>Basic usage</caption>
<search-modal
id="modal-search"
class="modal modal--search modal--top modal--blue"
aria-labelledby="modal-search-title"
aria-hidden="true"
>
<div class="modal__overlay" data-a11y-dialog-hide></div>
<div class="modal__wrapper" role="document">
<div class="modal__content">
<button
title="Close"
type="button"
class="modal__close"
aria-label="Close"
data-a11y-dialog-hide
>
<!-- Close icon -->
</button>
<search-form>
<form action="/search" method="get" class="search__form" role="search">
 <input
   id="modal-search-input"
   type="search"
   name="q"
   class="search__form-input"
   placeholder="Search"
   aria-label="Search"
   autofocus
 >
 <button type="submit" class="search__form-submit" aria-label="Submit search">
   <!-- Search icon -->
 </button>
</form>
</search-form>
</div>
</div>
</search-modal>
```


# staged-action

Staged Action

Controls the staged action state.

## Example

```html
<caption>Basic usage</caption>
<staged-action class="staged-action">
<staged-action-text class="staged-action__text">
{{ 'products.product.add_to_cart' | t }}
</staged-action-text>
<staged-action-tick class="staged-action__tick">
{% raw %}{% render 'icons-theme', icon: 'check %}{% endraw %}
</staged-action-tick>
<staged-action-spinner class="staged-action__spinner">
{% raw %}{% render 'theme-spinner' %}{% endraw %}
</staged-action-spinner>
</staged-action>
```

## Methods

| Method     | Type                        | Description                                      |
|------------|-----------------------------|--------------------------------------------------|
| `setState` | `(state?: string): Promise` | Set state<br /><br />**state**: State to set ('IDLE', 'DOING', 'DONE') |


# sticky-scroll

A custom element that provides a sticky scroll behavior, ensuring that it sticks to the top of the viewport with a specified gap.

## Attributes

| Attribute            | Type      | Description                          |
|----------------------|-----------|--------------------------------------|
| `data-sticky-header` | `boolean` | Whether the header should be sticky. |


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
{% raw %}{% render 'icons-theme', icon: 'close' %}{% endraw %}
</button>
<div
class="popup__content"
role="document"
>
{% raw %}{% render 'video-player',
id: video_player_id,
video_type: 'html5',
video: video_file,
poster_image_sizes: '(min-width: 990px) 990px, calc(100vw - 36px)'
%}{% endraw %}
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

A custom element that displays a collection of videos in a video gallery.

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
 {% raw %}{% render 'video-player',
   id: 'video-player-1',
   video_type: "youtube",
   external_video_id: "1234567789",
   poster_image: preview_image_object,
   poster_image_sizes: '(min-width: 1200px) 1200px, calc(100vw - 36px)'
 %}{% endraw %}
</video-gallery-slide>
<video-gallery-slide
 class="home-video__stage-video"
 id="video-gallery-slide--2"
>
 {% raw %}{% render 'video-player',
   id: 'video-player-2',
   video_type: "vimeo",
   external_video_id: "1234567789",
   poster_image_sizes: '(min-width: 1200px) 1200px, calc(100vw - 36px)'
 %}{% endraw %}
</video-gallery-slide>
<video-gallery-slide
 class="home-video__stage-video"
 id="video-gallery-slide--3"
>
 {% raw %}{% render 'video-player',
   id: 'video-player-1',
   video_type: 'html5',
   video: video,
   poster_image_sizes: '(min-width: 1200px) 1200px, calc(100vw - 36px)'
 %}{% endraw %}
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
   <div class="home-video__item-icon home-video__item-icon--play u-flex u-flex--middle u-flex--center">
     {%- assign icon_title = 'sections.video.play_label' | t -%}
     {% raw %}{%- render 'icons-theme', icon: 'play', title: icon_title -%}{% endraw %}
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
   <div class="home-video__item-icon home-video__item-icon--play u-flex u-flex--middle u-flex--center">
     {%- assign icon_title = 'sections.video.play_label' | t -%}
     {% raw %}{%- render 'icons-theme', icon: 'play', title: icon_title -%}{% endraw %}
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
     height="300"
   >
   <div class="home-video__item-img--overlay u-bg-overlay"></div>
   <div class="home-video__item-icon home-video__item-icon--play u-flex u-flex--middle u-flex--center">
     {%- assign icon_title = 'sections.video.play_label' | t -%}
     {% raw %}{%- render 'icons-theme', icon: 'play', title: icon_title -%}{% endraw %}
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

Video Gallery Thumbnail

A custom element that handles the display of a Vimeo video thumbnail in a video gallery.


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
{% raw %}{% render 'theme-spinner', tag: 'video-loading-indicator', hidden: true %}{% endraw %}
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

| Method        | Type                                             | Description                                      |
|---------------|--------------------------------------------------|--------------------------------------------------|
| `loadContent` | `(): VideoPlayer`                                | Load video content                               |
| `off`         | `(type: string, handler: Function, options?: string): VideoPlayer` | Remove event listener<br /><br />**type**: Event type<br />**handler**: Event handler<br />**options**: Event options |
| `on`          | `(type: string, handler: Function, options?: string): VideoPlayer` | Add event listener<br /><br />**type**: Event type<br />**handler**: Event handler<br />**options**: Event options |
| `pause`       | `(): VideoPlayer`                                | Pause video                                      |
| `play`        | `(): VideoPlayer`                                | Play video                                       |

## Events

| Event                   | Type               | Description                |
|-------------------------|--------------------|----------------------------|
| `on:video-player:ready` | `CustomEvent<any>` | Fired when player is ready |



[🔼 Back to top](#accordion)