---
description: 'simple animations library / author: sqwat'
---

# 📖 simple-animations

{% hint style="warning" %}
require("morion/simple-animations")
{% endhint %}

{% hint style="info" %}
the library allows you to easily make animations
{% endhint %}

### example of usage:

```lua
local animations = require("morion/simple-animations")

callbacks.init("on_paint", function()
    local alpha = animations.lerp("alpha", gvars.is_open_menu())
    
    draw.rect_filled(0, 0, 400, 400, color_rgba(255, 255, 255, math.floor(alpha*255)))
end)
```

### functions:

### lerp

`.lerp(id: string, value:boolean/number, [speed: number]):` <mark style="color:purple;">`number`</mark>

<table><thead><tr><th width="244.33333333333331">Name</th><th width="207">Type</th><th>Description</th></tr></thead><tbody><tr><td><strong>id</strong></td><td><strong><code>string</code></strong></td><td>unique animation id</td></tr><tr><td><strong>value</strong></td><td><strong><code>boolean/number</code></strong></td><td>animation value</td></tr><tr><td><strong>speed</strong></td><td><strong><code>number</code></strong></td><td>animation speed amount</td></tr></tbody></table>
