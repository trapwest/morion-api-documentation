# 🔌 callbacks

## how to use game events:

{% embed url="https://wiki.alliedmods.net/Counter-Strike:_Global_Offensive_Events" %}
Official CS:GO events
{% endembed %}

{% code lineNumbers="true" %}
```lua
callbacks.init("on_event", function(event)
    if (event:get_name() == "player_hurt") then
        --- code
    end
end)
```
{% endcode %}

## how to use callbacks:

### on\_paint

Fired every frame. Most functions from the [draw ](draw.md)namespace can only be used here.

{% code lineNumbers="true" %}
```lua
callbacks.init('on_paint', function()
    draw.rect_filled(200, 200, 100, 20, color_rgb(255, 255, 255, 255))
end)
```
{% endcode %}

### on\_createmove

Fired every time the game prepares a move command. Use the parameter passed by the callback to access the [`UserCmd`](callbacks-list.md#struct-usercmd).

{% code lineNumbers="true" %}
```lua
callbacks.init('on_createmove', function(cmd)
    cmd.viewangles.z = 50
end)
```
{% endcode %}

### after\_prediction

Use the parameter passed by the callback to access the [`UserCmd`](callbacks-list.md#struct-usercmd).

{% code lineNumbers="true" %}
```lua
callbacks.init('after_prediction', function(cmd)
    cmd.viewangles.z = 50
end)
```
{% endcode %}

#### 🔗 struct <mark style="color:blue;">`UserCmd`</mark>

| Name                | Type         | Description              |
| ------------------- | ------------ | ------------------------ |
| **forwardmove**     | **`number`** | Forward / backward speed |
| **sidemove**        | **`number`** | Left / right speed       |
| **upmove**          | **`number`** | Up / down speed          |
| **viewangles**      | **`vector`** | Player view angles       |
| **buttons**         | **`number`** | Player buttons           |
| **command\_number** | **`number`** | Current command number   |

### on\_frame\_net

{% hint style="info" %}
Stages - [enum\_frames.md](../enumerations/enum\_frames.md "mention")
{% endhint %}

{% code lineNumbers="true" %}
```lua
callbacks.init('on_frame_net', function(stage)
    if (stage == enum_frames.frame_start) then
        cheat.msg('frame_start')
    end
end)
```
{% endcode %}

### on\_override\_view

Fired every time the game prepares camera view.

{% code lineNumbers="true" %}
```lua
callbacks.init('on_override_view', function(view)
    view.fov = 20
end)
```
{% endcode %}

| Name               | Type         | Description |
| ------------------ | ------------ | ----------- |
| **fov**            | **`number`** | -           |
| **angles**         | **`vector`** | -           |
| **origin**         | **`vector`** | -           |
| **height**         | **`number`** | -           |
| **height\_old**    | **`number`** | -           |
| **width**          | **`number`** | -           |
| **width\_old**     | **`number`** | -           |
| **viewmodel\_fov** | **`number`** | -           |
| **x**              | **`number`** | -           |
| **x\_old**         | **`number`** | -           |
| **y**              | **`number`** | -           |
| **y\_old**         | **`number`** | -           |

### on\_unload

Fired when the script is about to unload.

{% code lineNumbers="true" %}
```lua
callbacks.init('on_unload', function()
    cheat.msg('Script unloaded!')
end)
```
{% endcode %}

### on\_shot

Fired every time the aimbot shoots at a player.

{% code lineNumbers="true" %}
```lua
callbacks.init('on_shot', function(shot_info)
    cheat.msg(shot_info.target_name)
end)
```
{% endcode %}

| Name               | Type          | Description                                |
| ------------------ | ------------- | ------------------------------------------ |
| **target\_name**   | **`string`**  | Target name                                |
| **target\_index**  | **`integer`** | Target index                               |
| **result**         | **`string`**  | Shot result                                |
| **client\_hitbox** | **`string`**  | Hitbox                                     |
| **server\_hitbox** | **`string`**  | Hitbox                                     |
| **client\_damage** | **`number`**  | Actual shot damage                         |
| **server\_damage** | **`number`**  | Actual shot damage                         |
| **hitchance**      | **`number`**  | Actual shot hit chance                     |
| **backtrack**      | **`number`**  | Amount of ticks the player was backtracked |
| **aim\_point**     | **`string`**  | Actual shot aim point                      |
