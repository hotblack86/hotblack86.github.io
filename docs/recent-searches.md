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
