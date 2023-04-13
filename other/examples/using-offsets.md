---
description: example of using offsets
---

# ⚙ using offsets

{% hint style="info" %}
to do something like this, you can refer to the [entity](../../documentation/namespaces/entity.md)
{% endhint %}

```lua
local font = draw.create_font("Verdana", 12)

callbacks.init("on_paint", function()
    local entities = entity.get_entities_by_classid(100) -- Inferno entity
    
    for i = 1, #entities do
       local inferno = entities[i]
       
       if inferno then 
          local origin = inferno:get_absorigin()
          local screen = draw.world_to_screen(origin)
        
          local inferno_spawn = inferno:get_offset(0x20)
          local inferno_spawn_time = inferno_spawn:get_float()
        
          draw.string(font, screen.x, screen.y, color_rgb(255, 255, 255), tostring(inferno_spawn_time), true)
       end
    end
end)
```
