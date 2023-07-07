---
description: drag and drop library
---

# 📖 drag-drop

{% hint style="warning" %}
require("morion/drag-drop")
{% endhint %}

{% hint style="info" %}
the library allows you to create draggable objects
{% endhint %}

### example of usage:

```lua
local dragging = require("morion/drag-drop")

local x_pos = ui:new_slider_int("x pos", 50, engine.get_screen_size( ).x)
local y_pos = ui:new_slider_int("y pos", 50, engine.get_screen_size( ).y)

local new_drag_obj = dragging.push({ x, y }, vector_2d(100, 100), "new-object", function(self)
    draw.rect_filled( self.position.x, self.position.y, self.size.x, self.size.y, color_rgb(255, 255, 255) )
end)

callbacks.init("on_paint", function()
    new_drag_obj:draw()

    -- saving x & y for new_drag_obj
    for k, v in pairs(new_drag_obj:get_elements()) do
        v:set( k == "x" and new_drag_obj:get_position().x or new_drag_obj:get_position().y )
    end
end)
```

### functions:

### push

`.push(xy: table, size: vector_2d, name: string, draw: function):` <mark style="color:purple;">`drag_elem`</mark>

### classes:

### draw

<mark style="color:purple;">`<drag_elem>`</mark>`:draw()`

drawing draggable element

### get\_elements

<mark style="color:purple;">`<drag_elem>`</mark>`:get_elements()` <mark style="color:purple;">`array of 'menu_element'`</mark>

returns gui elements from draggable element

### get\_position

<mark style="color:purple;">`<drag_elem>`</mark>`:get_position()` <mark style="color:purple;">`vector_2d`</mark>

returns draggable element position
