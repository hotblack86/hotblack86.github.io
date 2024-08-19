# accordion

Accordion class to handle the opening and closing of a single accordion item.

## Properties

| Property      | Type         | Default |
|---------------|--------------|---------|
| `animation`   |              | null    |
| `content`     | `any \| any` |         |
| `el`          |              | "el"    |
| `isClosing`   | `boolean`    | false   |
| `isExpanding` | `boolean`    | false   |
| `summary`     | `any \| any` |         |

## Methods

| Method              | Type                    | Description                                      |
|---------------------|-------------------------|--------------------------------------------------|
| `expand`            | `(): void`              | Expands the accordion with an animation.         |
| `onAnimationFinish` | `(open: boolean): void` | Finishes the animation and resets the state of the accordion.<br /><br />**open**: Whether the accordion should be open. |
| `onClick`           | `(e: MouseEvent): void` | Handles the click event on the accordion summary element.<br /><br />**e**: The click event. |
| `open`              | `(): void`              | Opens the accordion.                             |
| `shrink`            | `(): void`              | Initiates the closing animation of the accordion. |

## Events

| Event                    | Type               | Description                                    |
|--------------------------|--------------------|------------------------------------------------|
| `on:accordion:cancelled` | `CustomEvent<any>` | Fires when an ongoing animation is canceled.   |
| `on:accordion:closed`    | `CustomEvent<any>` | Fires when the accordion has finished closing. |
| `on:accordion:closing`   | `CustomEvent<any>` | Fires when the accordion begins to close.      |
| `on:accordion:opened`    | `CustomEvent<any>` | Fires when the accordion has finished opening. |
| `on:accordion:opening`   | `CustomEvent<any>` | Fires when the accordion begins to open.       |


# accordion-group

AccordionGroup class to manage multiple accordions within a group.

## Attributes

| Attribute    | Type      | Description                                      |
|--------------|-----------|--------------------------------------------------|
| `alwaysOpen` | `boolean` | If true, ensures at least one accordion is always open. |
| `singleOpen` | `boolean` | If true, only one accordion in the group can be open at a time. |

## Methods

| Method  | Type                 | Description                                      |
|---------|----------------------|--------------------------------------------------|
| `close` | `(id: string): void` | Closes the accordion with the given ID.<br /><br />**id**: The ID of the accordion to close. |
| `open`  | `(id: string): void` | Opens the accordion with the given ID.<br /><br />**id**: The ID of the accordion to open. |
