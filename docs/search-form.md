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
{% render 'icons-theme', icon: 'search' %}
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
