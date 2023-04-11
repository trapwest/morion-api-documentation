# 📃 enum\_frames

### example <a href="#example" id="example"></a>

{% code lineNumbers="true" %}
```lua
callbacks.init('on_frame_net', function(stage)
    if stage == enum_frames.frame_start then

    end
end)
```
{% endcode %}

## entries <a href="#entries" id="entries"></a>

| Value                                     |
| ----------------------------------------- |
| frame\_start                              |
| frame\_net\_update\_start                 |
| frame\_net\_update\_end                   |
| frame\_net\_update\_postdataupdate\_start |
| frame\_net\_update\_postdataupdate\_end   |
| frame\_render\_start                      |
| frame\_render\_end                        |
