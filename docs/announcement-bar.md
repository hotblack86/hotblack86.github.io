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
