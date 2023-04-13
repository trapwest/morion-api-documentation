---
description: example of gui interaction
---

# ⚙ gui interaction

{% hint style="info" %}
to do something like this, you can refer to the [gui](../../documentation/namespaces/gui.md)
{% endhint %}

<pre class="language-lua"><code class="lang-lua"><strong>local cui = gui.begin({"Group 1", "Group 2", "Group 3", "Group 4"})
</strong>
local new_box = cui:new_checkbox("New box")
local new_slider_float = cui:new_slider_float("New slider float", 0, 100)
local new_slider_int = cui:new_slider_int("New slider int", 0, 100)
local new_label = cui:new_label("New label")
local new_button = cui:new_button("New button")
local new_combo = cui:new_combo("New combo", { "Element 1", "Element 2", "Element 3" })
local new_list = cui:new_list("New list", { "Element 1", "Element 2", "Element 3" })
local new_input = cui:new_input("New input")

new_box:set_group("Group 2")
new_button:set_group("Group 3")
new_list:set_group("Group 4")

new_box:set_tooltip("Simple checkbox")

callbacks.init("on_paint", function()
    new_box:set_callback(function()
        cheat.msg( "callback active" )
    end)
end)
</code></pre>
