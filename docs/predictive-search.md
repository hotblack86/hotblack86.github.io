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
