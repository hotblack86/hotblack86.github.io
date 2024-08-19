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
