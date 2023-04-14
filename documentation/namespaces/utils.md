# 🪛 utils

### get\_choked\_commands

`utils.get_choked_commands():` <mark style="color:purple;">`number`</mark>

Returns the number of choked commands.

### get\_clipboard

`utils.get_clipboard():` <mark style="color:purple;">`string`</mark>

Returns from the clipboard.

### set\_clipboard

`utils.set_clipboard(text: string)`

| Name     | Type         | Description |
| -------- | ------------ | ----------- |
| **text** | **`string`** | text        |

Sets the text to the clipboard.

### get\_active\_key

{% embed url="https://docs.microsoft.com/en-us/windows/win32/inputdev/virtual-key-codes" %}

`utils.get_active_key(key: number):` <mark style="color:purple;">`boolean`</mark>

| Name    | Type         | Description  |
| ------- | ------------ | ------------ |
| **key** | **`number`** | Key to check |

Returns <mark style="color:green;">`true`</mark>, if the button is active.

### get\_cursor\_position

`utils.get_cursor_position():` <mark style="color:purple;">`vector_2d`</mark>

Returns the current mouse position.

### set\_cursor\_visible

`utils.set_cursor_visible(visible: boolean)`

| Name     | Type         | Description |
| -------- | ------------ | ----------- |
| **visible** | **`boolean`** | cursor visible        |

Sets the cursor visible.

### get\_scroll

`utils.get_scroll():` <mark style="color:purple;">`number`</mark>

Returns <mark style="color:blue;">`-1.0`</mark> if the mouse wheel is spinning down, <mark style="color:blue;">`1.0`</mark> if the mouse wheel is spinning up, and <mark style="color:blue;">`0.0`</mark> if the mouse wheel is not rotating.
