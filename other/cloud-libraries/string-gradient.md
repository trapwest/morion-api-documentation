---
description: 'string gradient library / author: Klient'
---

# 📖 string-gradient

{% hint style="warning" %}
require("morion/string-gradient")
{% endhint %}

{% hint style="info" %}
the library allows you to create text with a gradient effect.

_you can use it anywhere: gui, render and etc._
{% endhint %}

### example of usage:

```lua
local string_gradient = require("morion/string-gradient")

local ui = gui.begin({ "main" })
local checkbox = ui:new_checkbox(string_gradient.format("my element", { 
        color_rgb(255, 0, 0),
        color_rgb(0, 255, 0),
        color_rgb(0, 0, 255)
}))
```

### functions:

### format

`.format(text: string, colors: table):` <mark style="color:purple;">`string`</mark>

<table><thead><tr><th width="244.33333333333331">Name</th><th width="207">Type</th><th>Description</th></tr></thead><tbody><tr><td><strong>text</strong></td><td><strong><code>string</code></strong></td><td>text for formatting</td></tr><tr><td><strong>colors</strong></td><td><strong><code>table</code></strong></td><td>table of colors</td></tr></tbody></table>
