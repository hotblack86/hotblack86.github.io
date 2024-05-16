# nested-menu

## Properties

| Property           | Type               |
|--------------------|--------------------|
| `menu`             | `any \| any`       |
| `rows`             | `array`            |
| `submenuDirection` | `string`           |
| `submenus`         | `array`            |
| `tolerance`        | `string \| number` |

## Methods

| Method                | Type                                  | Description                                      |
|-----------------------|---------------------------------------|--------------------------------------------------|
| `#activationDelay`    | `(): number`                          | Return the amount of time that should be used as a delay before the<br />currently hovered row is activated.<br /><br />Returns 0 if the activation should happen immediately. Otherwise,<br />returns the number of milliseconds that should be delayed before<br />checking again to see if the row should be activated. |
| `#clickRow`           | `(e: any): void`                      | Immediately activate a row if the user clicks on it. |
| `#mouseenterRow`      | `(e: any): void`                      | Trigger a possible row activation whenever entering a new row. |
| `#mouseleaveMenu`     | `(): void`                            | Cancel possible row activations when leaving the menu entirely |
| `#mousemoveDocument`  | `(e: any): void`                      | Keep track of the last few locations of the mouse. |
| `#possiblyActivate`   | `(row: any): void`                    | Possibly activate a menu row. If mouse movement indicates that we<br />shouldn't activate yet because user may be trying to enter<br />a submenu's content, then delay and check again later. |
| `#possiblyDeactivate` | `(row: any, initialDelay: any): void` | Possibly deactivate a menu row. If mouse movement indicates that we<br />shouldn't deactivate yet because user may be trying to enter<br />a submenu's content, then delay and check again later. |
| `activate`            | `(row: any): void`                    | Activate a menu row.                             |
