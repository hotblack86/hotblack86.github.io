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
