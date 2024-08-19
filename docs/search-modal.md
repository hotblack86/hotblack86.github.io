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
