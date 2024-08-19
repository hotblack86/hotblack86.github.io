# countdown-timer

Countdown timer web component

This component displays a countdown timer and provides options to handle the completion
of the countdown in various ways, such as hiding the component or showing a custom message.

## Example

```html
<caption>Basic usage</caption>
<countdown-timer
year="2024"
month="5"
day="17"
hour="12"
minute="0"
completion="zero-with-message"
completion-message="The countdown is complete!"
>
<div id="days" class="countdown__segment">
<span class="countdown__label">Days</span>
<span class="countdown__value">00</span>
</div>
<div id="hours" class="countdown__segment">
<span class="countdown__label">Hours</span>
<span class="countdown__value">00</span>
</div>
<div id="minutes" class="countdown__segment">
<span class="countdown__label">Minutes</span>
<span class="countdown__value">00</span>
</div>
<div id="seconds" class="countdown__segment">
<span class="countdown__label">Seconds</span>
<span class="countdown__value">00</span>
</div>
</countdown-timer>
```

## Attributes

| Attribute            | Type     | Description                                      |
|----------------------|----------|--------------------------------------------------|
| `completion-message` | `string` | The message to display upon countdown completion if 'zero-with-message' is set |

## Properties

| Property            | Attribute    | Type            | Default | Description                                      |
|---------------------|--------------|-----------------|---------|--------------------------------------------------|
| `completion`        | `completion` | `string`        |         | The action to take upon countdown completion ('hide' or 'zero-with-message') |
| `completionMessage` |              | `string \| any` |         |                                                  |
| `day`               | `day`        | `string`        |         | The target day for the countdown                 |
| `daysElement`       |              | `any \| any`    |         |                                                  |
| `hour`              | `hour`       | `string`        |         | The target hour for the countdown                |
| `hoursElement`      |              | `any \| any`    |         |                                                  |
| `intervalId`        |              |                 | null    |                                                  |
| `minute`            | `minute`     | `string`        |         | The target minute for the countdown              |
| `minutesElement`    |              | `any \| any`    |         |                                                  |
| `month`             | `month`      | `string`        |         | The target month for the countdown (1-12)        |
| `secondsElement`    |              | `any \| any`    |         |                                                  |
| `year`              | `year`       | `string`        |         | The target year for the countdown                |

## Methods

| Method                 | Type                                             | Description                                      |
|------------------------|--------------------------------------------------|--------------------------------------------------|
| `#dispatchEvent`       | `(name: string, detail?: string): void`          | Dispatch a custom event.<br /><br />**name**: The name of the event.<br />**detail**: Additional event detail data. |
| `#displayCountdown`    | `(days: string, hours: string, minutes: string, seconds: string): void` | Display the countdown values in the respective elements.<br /><br />**days**: The days value to display.<br />**hours**: The hours value to display.<br />**minutes**: The minutes value to display.<br />**seconds**: The seconds value to display. |
| `#parseAttributeToInt` | `(attrName: string, defaultValue: number): number` | Parse an attribute value to an integer.<br /><br />**attrName**: The name of the attribute.<br />**defaultValue**: The default value to return if parsing fails. |
| `handleCompletion`     | `(): void`                                       | Handle the completion of the countdown.<br /><br />This method performs the specified completion action, such as hiding the<br />parent element or displaying a completion message. |
| `updateCountdown`      | `(): void`                                       | Update the countdown timer.<br /><br />This method calculates the time remaining until the target date and<br />updates the display accordingly. If the countdown is complete, it<br />handles the completion behavior and fires the appropriate events. |

## Events

| Event                    | Description                                      |
|--------------------------|--------------------------------------------------|
| `on:countdown:completed` | Fired when the countdown completes.              |
| `on:countdown:tick`      | Fired every second with the updated countdown values. |

## CSS Custom Properties

| Property                       | Description                |
|--------------------------------|----------------------------|
| `--countdown-background-color` | Countdown background color |
| `--countdown-color`            | Countdown text color       |
