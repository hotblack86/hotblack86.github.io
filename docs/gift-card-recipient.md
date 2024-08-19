# gift-card-recipient

A custom element that manages the activation of a fieldset based on a checkbox.
When the checkbox is checked, it enables and reveals the associated fields.
When unchecked, it disables and hides them.

## Properties

| Property   | Type                  |
|------------|-----------------------|
| `checkbox` | `any \| any`          |
| `fields`   | `NodeListOf<Element>` |
| `fieldset` | `any \| any`          |

## Methods

| Method             | Type       | Description                                      |
|--------------------|------------|--------------------------------------------------|
| `activateFieldset` | `(): void` | Activates or deactivates the fieldset based on the checkbox's checked state.<br />Enables and reveals the fields if the checkbox is checked,<br />otherwise, disables and hides them. |
