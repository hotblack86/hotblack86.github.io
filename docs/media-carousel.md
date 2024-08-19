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
{%- render 'icons-theme', icon: 'chevron, additional_classes: 'icon--left' -%}
</button>
<button
class="
media-gallery__arrow
media-gallery__arrow--next
js-carousel-next
"
>
{%- render 'icons-theme', icon: 'chevron -%}
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
