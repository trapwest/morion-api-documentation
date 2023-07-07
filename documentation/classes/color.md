# 🎨 color

{% tabs %}
{% tab title="color_rgb" %}
`color_rgb(r: number, g: number, b: number)`
{% endtab %}

{% tab title="color_rgba" %}
`color_rgba(r: number, g: number, b: number, a: number)`
{% endtab %}
{% endtabs %}

### structure:

| Name | Type   | Description |
| ---- | ------ | ----------- |
| r    | number | red         |
| g    | number | green       |
| b    | number | blue        |
| a    | number | alpha       |
| hex  | string | hex         |

### override\_alpha:

`<color>:override_alpha(alpha: number):` <mark style="color:purple;">`color`</mark>

returns the current color with a different transparency value

### using:

```lua
local col_f = color_rgb(255, 255, 255)
local col_s = color_rgba(255, 255, 255, 255)

local r, g, b, a, hex = col_f:r(), col_f:g(), col_f:b(), col_f:a(), col_f:hex()
```
