Add a [backdrop-filter](https://developer.mozilla.org/en-US/docs/Web/CSS/backdrop-filter) behind the Home Assistant popups.

{% if installed %}
## Installation
Then, configured as `type: module` in your Lovelace yaml config.
```yaml
resources:
  - url: /community_plugin/popup-backdrop-filter/popup-backdrop-filter.js
    type: module
```

This repo can also be downloaded and the CSS loaded into Lovelace, but that will not provide future updates since HACS currently does not support a CSS type.

## Theme Variables
This adds a single CSS variable which can be changed in the current theme configuration. The popup background color can also be changed via the default [iron-overlay](https://www.webcomponents.org/element/@polymer/iron-overlay-behavior) configuration.

| Property                                 | Description                                                                                                                                                     | Default           |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|
| `iron-overlay-backdrop-filter`           | Backdrop filter                                                                                                                                                 | `blur(10px)`      |
| `iron-overlay-backdrop-background-color` | Backdrop background color. Use `rgba` so that the background is see-through.                                                                                    | `rgba(0,0,0,0.25)` |
| `iron-overlay-backdrop-opacity`          | Backdrop opacity. This differs from using `rgba` on the background-color in that is actually makes the entire blur less opaque. This can create a foggy effect. | `1`               |

## Example Theme Config
```yaml
  iron-overlay-backdrop-filter: 'blur(10px) grayscale(50%)'
  iron-overlay-backdrop-background-color: 'rgba(41,128,185,0.25)'
```
{% endif %}
