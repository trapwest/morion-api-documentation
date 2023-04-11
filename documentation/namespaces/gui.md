# 💻 gui

{% hint style="info" %}
available examples: [gui interaction](../../other/examples/gui-interaction.md)
{% endhint %}

## functions:

### menu\_bool

`gui.menu_bool(name: string):` <mark style="color:purple;">`menu_element`</mark>

| Name     | Type         | Description         |
| -------- | ------------ | ------------------- |
| **name** | **`string`** | The needed element. |

Returns an item from the menu that has been assigned the boolean data type.

### menu\_int

`gui.menu_int(name: string):` <mark style="color:purple;">`menu_element`</mark>

| Name     | Type         | Description         |
| -------- | ------------ | ------------------- |
| **name** | **`string`** | The needed element. |

Returns an item from the menu that has been assigned the integer data type.

### menu\_float

`gui.menu_float(name: string):` <mark style="color:purple;">`menu_element`</mark>

| Name     | Type         | Description         |
| -------- | ------------ | ------------------- |
| **name** | **`string`** | The needed element. |

Returns an item from the menu that has been assigned the float data type.

### menu\_color

`gui.menu_float(name: string):` <mark style="color:purple;">`menu_element`</mark>

| Name     | Type         | Description         |
| -------- | ------------ | ------------------- |
| **name** | **`string`** | The needed element. |

Returns an item from the menu that has been assigned the color data type.

### get\_bind\_mode

`gui.get_bind_mode(name: string):` <mark style="color:purple;">`number`</mark>

| Name     | Type         | Description         |
| -------- | ------------ | ------------------- |
| **name** | **`string`** | The needed element. |

Returns the mode of the bind.

### get\_bind\_state

`gui.get_bind_state(name: string):` <mark style="color:purple;">`boolean`</mark>

| Name     | Type         | Description         |
| -------- | ------------ | ------------------- |
| **name** | **`string`** | The needed element. |

Returns the state of the bind.

### set\_bind\_state

`gui.get_bind_state(name: string, state: boolean)`

| Name      | Type          | Description                              |
| --------- | ------------- | ---------------------------------------- |
| **name**  | **`string`**  | The needed element.                      |
| **state** | **`boolean`** | The state to which the bind will be set. |

Sets the value of the bind.

### begin

{% tabs %}
{% tab title="groups" %}
`gui.begin(groups: {, ...}):` <mark style="color:purple;">`gui_group`</mark> <mark style="color:purple;">`maximum: 4`</mark>

| Name       | Type         | Description        |
| ---------- | ------------ | ------------------ |
| **groups** | **`string`** | Table with groups. |

Creates a group with gui elements.

<figure><img src="../../.gitbook/assets/asdasd.png" alt=""><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}

## 🔗 <mark style="color:blue;">`gui_group`</mark>

### :new\_checkbox

`group:new_checkbox(name: string):` <mark style="color:purple;">`menu_element`</mark>

| Name     | Type         | Description   |
| -------- | ------------ | ------------- |
| **name** | **`string`** | Element name. |

### :new\_input

`group:new_input(name: string):` <mark style="color:purple;">`menu_element`</mark>

| Name     | Type         | Description   |
| -------- | ------------ | ------------- |
| **name** | **`string`** | Element name. |

### :new\_bind

`group:new_bind(name: string):` <mark style="color:purple;">`menu_element`</mark>

| Name     | Type         | Description   |
| -------- | ------------ | ------------- |
| **name** | **`string`** | Element name. |

### :new\_combo

`group:new_combo(name: string, items: {, ...}):` <mark style="color:purple;">`menu_element`</mark>

| Name      | Type         | Description   |
| --------- | ------------ | ------------- |
| **name**  | **`string`** | Element name. |
| **items** | **`string`** | Combo items.  |

### :new\_slider\_int

`group:new_slider_int(name: string, min: number, max: number):` <mark style="color:purple;">`menu_element`</mark>

| Name     | Type         | Description            |
| -------- | ------------ | ---------------------- |
| **name** | **`string`** | Element name.          |
| **min**  | **`number`** | Minimum allowed value. |
| **min**  | **`number`** | Maximum allowed value. |

### :new\_slider\_float

`group:new_slider_float(name: string, min: number, max: number):` <mark style="color:purple;">`menu_element`</mark>

| Name     | Type         | Description            |
| -------- | ------------ | ---------------------- |
| **name** | **`string`** | Element name.          |
| **min**  | **`number`** | Minimum allowed value. |
| **min**  | **`number`** | Maximum allowed value. |

### :new\_button

`group:new_button(name: string):` <mark style="color:purple;">`menu_element`</mark>

| Name     | Type         | Description   |
| -------- | ------------ | ------------- |
| **name** | **`string`** | Element name. |

### :new\_color

`group:new_color(name: string):` <mark style="color:purple;">`menu_element`</mark>

| Name     | Type         | Description   |
| -------- | ------------ | ------------- |
| **name** | **`string`** | Element name. |

### :new\_label

`group:new_label(name: string):` <mark style="color:purple;">`menu_element`</mark>

| Name     | Type         | Description   |
| -------- | ------------ | ------------- |
| **name** | **`string`** | Element name. |

### :new\_list

`group:new_list(name: string, items: {, ...}):` <mark style="color:purple;">`menu_element`</mark>

| Name      | Type         | Description   |
| --------- | ------------ | ------------- |
| **name**  | **`string`** | Element name. |
| **items** | **`string`** | List items.   |

## 🔗 <mark style="color:blue;">`menu_element`</mark>

### :get

`element:get():` <mark style="color:purple;">`any`</mark>

Returns the value of the menu element.

### :get\_type

`element:get_type():` <mark style="color:purple;">`string`</mark>

Returns the type of the menu element.

### :get\_name

`element:get_name():` <mark style="color:purple;">`string`</mark>

Returns the name of the menu element.

### :get\_items

`element:get_items():` <mark style="color:purple;">`table`</mark>

Returns the list of items. [`new_combo`](gui.md#new\_combo) / [`new_list`](gui.md#new\_label) menu element objects only.

### :get\_mode

`element:get_mode():` <mark style="color:purple;">`number`</mark>

Returns the current keybind mode. [`new_bind`](gui.md#new\_bind) menu element objects only.

### :set

`element:set(value: any)`

| Name      | Type      | Description                                      |
| --------- | --------- | ------------------------------------------------ |
| **value** | **`any`** | The value to which the menu element will be set. |

Sets the value of the menu element.

### :set\_items

`element:set_items(items: {, ...})`

| Name      | Type         | Description               |
| --------- | ------------ | ------------------------- |
| **items** | **`string`** | Table with string values. |

Sets a table with items. [`new_combo`](gui.md#new\_combo) / [`new_list`](gui.md#new\_list) menu element objects only.

### :set\_tooltip

`element:set_tooltip(text: string)`

| Name      | Type         | Description   |
| --------- | ------------ | ------------- |
| **value** | **`string`** | Tooltip text. |

Sets the tooltip of the menu element.

### :set\_visible

`element:set_visible(state: boolean)`

| Name      | Type          | Description       |
| --------- | ------------- | ----------------- |
| **state** | **`boolean`** | Visibility state. |

Sets the menu element visibility.

### :set\_callback

`element:set_callback(callback: function)`

| Name         | Type           | Description                                                         |
| ------------ | -------------- | ------------------------------------------------------------------- |
| **callback** | **`function`** | Function that will be called when the menu item is interacted with. |

Sets the callback to the specified menu element.

### :set\_group

`element:set_group(group: string)`

| Name      | Type         | Description |
| --------- | ------------ | ----------- |
| **group** | **`string`** | Group name. |

Sets the group to the specified menu element.
