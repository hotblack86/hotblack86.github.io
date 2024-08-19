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
