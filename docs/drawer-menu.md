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
