# 🗺 draw

## Functions:

### world\_to\_screen

`draw.world_to_screen(position: vector):` <mark style="color:purple;">`vector`</mark>

| Name         | Type         | Description              |
| ------------ | ------------ | ------------------------ |
| **position** | **`vector`** | Position in world space. |

Returns the screen position vector. This can only be called from the on\_paint callback.

### create\_font

`draw.create_font(name: string, size: number, flags: number):` <mark style="color:purple;">`font_object`</mark>

| Name      | Type         | Description                                          |
| --------- | ------------ | ---------------------------------------------------- |
| **name**  | **`string`** | Font that will be initialized.                       |
| **size**  | **`number`** | Size of the font.                                    |
| **flags** | **`number`** | [`font_flags`](../enumerations/use\_font\_flags.md). |

Returns the [<mark style="color:blue;">`font_object`</mark>](draw.md#font\_object) struct or nil on failure.

### create\_weapon\_font

`draw.create_weapon_font(size: number):` <mark style="color:purple;">`font_object`</mark>

| Name     | Type         | Description       |
| -------- | ------------ | ----------------- |
| **size** | **`number`** | Size of the font. |

Returns the [<mark style="color:blue;">`font_object`</mark>](draw.md#font\_object) struct or nil on failure.

### create\_texture

`draw.create_texture(path: string):` <mark style="color:purple;">`texture`</mark>

| Name     | Type         | Description        |
| -------- | ------------ | ------------------ |
| **path** | **`string`** | Path to the image. |

Returns the <mark style="color:purple;">`texture`</mark> or nil on failure.

### get\_text\_size

`draw.get_text_size(font: font_object, text: string):` <mark style="color:purple;">`vector`</mark>

| Name     | Type              | Description                                |
| -------- | ----------------- | ------------------------------------------ |
| **font** | **`font_object`** | Font.                                      |
| **text** | **`string`**      | Text from which the size will be obtained. |

Returns the size of the text.

## Structs

### 🔗 <mark style="color:blue;">`font_object`</mark>

#### size

`font.size:` <mark style="color:purple;">`number`</mark>

## Draw functions

### blur

`draw.blur(x: number, y: number: width: number, height: number, alpha: number)`

| Name       | Type         | Description |
| ---------- | ------------ | ----------- |
| **x**      | **`number`** | X position. |
| **y**      | **`number`** | Y position. |
| **width**  | **`number`** | Width.      |
| **height** | **`number`** | Height.     |
| **alpha**  | **`number`** | Alpha.      |

### line

`draw.line(x: number, y: number, x2: number, y2: number, color: color, thickness: number)`

| Name        | Type         | Description            |
| ----------- | ------------ | ---------------------- |
| **x**       | **`number`** | X position.            |
| **y**       | **`number`** | Y position.            |
| **x2**      | **`number`** | Second X position.     |
| **y2**      | **`number`** | Second Y position.     |
| **color**   | **`color`**  | Color of the line.     |
| **thickne** | **`number`** | Thickness of the line. |

### polygon

`draw.polygon(color: color, positions: {, ...})`

| Name          | Type         | Description           |
| ------------- | ------------ | --------------------- |
| **color**     | **`color`**  | Color of the polygon. |
| **positions** | **`vector`** | Screen positions.     |

### polyline

`draw.polyline(color: color, closed: boolean, thickness: number, positions: {, ...})`

| Name          | Type          | Description                        |
| ------------- | ------------- | ---------------------------------- |
| **color**     | **`color`**   | Color of the polygon.              |
| **closed**    | **`boolean`** | Connects the end to the beginning. |
| **thickness** | **`number`**  | Thickness of the polyline.         |
| **positions** | **`vector`**  | Screen positions.                  |

### rect

`draw.rect(x: number, y: number, width: number, height: number, color: color[, rounding: number, rounding_corners: number])`

| Name                  | Type         | Description                                                                      |
| --------------------- | ------------ | -------------------------------------------------------------------------------- |
| **x**                 | **`number`** | X position.                                                                      |
| **y**                 | **`number`** | Y position.                                                                      |
| **width**             | **`number`** | Width.                                                                           |
| **height**            | **`number`** | Height.                                                                          |
| **color**             | **`color`**  | Color of the rectangle.                                                          |
| **rounding**          | **`number`** | Optional. Rounding of the rectangle in pixels.                                   |
| **rounding\_corners** | **`number`** | Optional. Rounds off certain corners. [`rounding`](../enumerations/rounding.md)  |

### rect\_filled

`draw.rect_filled(x: number, y: number, width: number, height: number, color: color[, rounding: number, rounding_corners: number])`

| Name                  | Type         | Description                                                                      |
| --------------------- | ------------ | -------------------------------------------------------------------------------- |
| **x**                 | **`number`** | X position.                                                                      |
| **y**                 | **`number`** | Y position.                                                                      |
| **width**             | **`number`** | Width.                                                                           |
| **height**            | **`number`** | Height.                                                                          |
| **color**             | **`color`**  | Color of the rectangle.                                                          |
| **rounding**          | **`number`** | Optional. Rounding of the rectangle in pixels.                                   |
| **rounding\_corners** | **`number`** | Optional. Rounds off certain corners. [`rounding`](../enumerations/rounding.md). |

### gradient

`draw.gradient(x: number, y: number, width: number, height: number, first_color: color, second_color[, type: number])`

| Name              | Type         | Description                                                                                                       |
| ----------------- | ------------ | ----------------------------------------------------------------------------------------------------------------- |
| **x**             | **`number`** | X position.                                                                                                       |
| **y**             | **`number`** | Y position.                                                                                                       |
| **width**         | **`number`** | Width.                                                                                                            |
| **height**        | **`number`** | Height.                                                                                                           |
| **first\_color**  | **`color`**  | First color.                                                                                                      |
| **second\_color** | **`color`**  | Second color.                                                                                                     |
| **type**          | **`number`** | Optional. <mark style="color:purple;">`0`</mark> - horizontal, <mark style="color:purple;">`1`</mark> - vertical. |

### circle

`draw.circle(x: number, y: number, points: number, radius: number, color: color)`

| Name       | Type         | Description           |
| ---------- | ------------ | --------------------- |
| **x**      | **`number`** | X position.           |
| **y**      | **`number`** | Y position.           |
| **points** | **`number`** | Points of the circle. |
| **radius** | **`number`** | Radius of the circle. |
| **color**  | **`color`**  | Color of the circle.  |

### circle\_filled

`draw.circle_filled(x: number, y: number, points: number, radius: number, color: color)`

| Name       | Type         | Description           |
| ---------- | ------------ | --------------------- |
| **x**      | **`number`** | X position.           |
| **y**      | **`number`** | Y position.           |
| **points** | **`number`** | Points of the circle. |
| **radius** | **`number`** | Radius of the circle. |
| **color**  | **`color`**  | Color of the circle.  |

### glow\_circle

`draw.glow_circle(x: number, y: number, radius: number, color: color)`

| Name       | Type         | Description           |
| ---------- | ------------ | --------------------- |
| **x**      | **`number`** | X position.           |
| **y**      | **`number`** | Y position.           |
| **radius** | **`number`** | Radius of the circle. |
| **color**  | **`color`**  | Color of the circle.  |

### arc

`draw.arc(x: number, y: number, radius: number, second_radius: number, min: number, max: number, color: color)`

| Name               | Type         | Description                  |
| ------------------ | ------------ | ---------------------------- |
| **x**              | **`number`** | X position.                  |
| **y**              | **`number`** | Y position.                  |
| **radius**         | **`number`** | Radius of the circle.        |
| **second\_radius** | **`number`** | Second radius of the circle. |
| **min**            | **`number`** | Minimum value.               |
| **max**            | **`number`** | Maximum value.               |
| **color**          | **`color`**  | Color of the arc.            |

### circle\_3d

`draw.circle_3d(position: vector, radius: number, color: color)`

| Name         | Type         | Description           |
| ------------ | ------------ | --------------------- |
| **position** | **`vector`** | Screen position.      |
| **radius**   | **`number`** | Radius of the circle. |
| **colorgs**  | **`color`**  | Color of the circle.  |

### circle\_filled\_3d

`draw.circle_filled_3d(position: vector, radius: number, color: color)`

| Name         | Type         | Description           |
| ------------ | ------------ | --------------------- |
| **position** | **`vector`** | Screen position.      |
| **radius**   | **`number`** | Radius of the circle. |
| **colorgs**  | **`color`**  | Color of the circle.  |

### string

{% hint style="info" %}
Render any text via the [`create_font` ](draw.md#create\_font)or [`create_weapon_font`](draw.md#create\_weapon\_font) function.
{% endhint %}

`draw.string(font: font_object, x: number, y: number, color: color, text: string[, shadow: boolean, outline: boolean])`

| Name        | Type              | Description              |
| ----------- | ----------------- | ------------------------ |
| **font**    | **`font_object`** | Font.                    |
| **x**       | **`number`**      | X position.              |
| **y**       | **`number`**      | Y position.              |
| **color**   | **`color`**       | Color of the text.       |
| **text**    | **`string`**      | Text that will be drawn. |
| **shadow**  | **`boolean`**     | Optional. Text shadow.   |
| **outline** | **`boolean`**     | Optional. Text outline.  |

### gradient\_string

{% hint style="info" %}
Render any text via the [`create_font` ](draw.md#create\_font)or [`create_weapon_font`](draw.md#create\_weapon\_font) function.
{% endhint %}

`draw.gradient_string(font: font_object, x: number, y: number, color: color, second_color: color, text: string, smooth: number[, shadow: boolean, outline: boolean])`

| Name              | Type              | Description                 |
| ----------------- | ----------------- | --------------------------- |
| **font**          | **`font_object`** | Font.                       |
| **x**             | **`number`**      | X position.                 |
| **y**             | **`number`**      | Y position.                 |
| **color**         | **`color`**       | Color of the text.          |
| **second\_color** | **`color`**       | Second color of the text.   |
| **text**          | **`string`**      | Text that will be drawn.    |
| **smooth**        | **`number`**      | Smoothness of the gradient. |
| **shadow**        | **`boolean`**     | Optional. Text shadow.      |
| **outline**       | **`boolean`**     | Optional. Text outline.     |

### image\_uv

`draw.image_uv(texture: texture, position: vector, size: vector, display_min: vector, display_size: vector, texture_size: vector, color: color[, rounding: number])`

| Name              | Type          | Description               |
| ----------------- | ------------- | ------------------------- |
| **texture**       | **`texture`** | Texture.                  |
| **position**      | **`vector`**  | Position.                 |
| **size**          | **`vector`**  | Size.                     |
| **display\_min**  | **`vector`**  | None.                     |
| **second\_color** | **`number`**  | None.                     |
| **color**         | **`color`**   | Color of the image.       |
| **rounding**      | **`number`**  | Optional. Image rounding. |

### image\_quad

`draw.image_quad(texture: texture, pos1: vector_2d, pos2: vector_2d, pos3: vector_2d, pos4: vector_2d[, color: color, rounding: number])`

| Name         | Type            | Description                   |
| ------------ | --------------- | ----------------------------- |
| **texture**  | **`texture`**   | Texture.                      |
| **pos1**     | **`vector_2d`** | First position.               |
| **pos2**     | **`vector_2d`** | Second position.              |
| **pos3**     | **`vector_2d`** | Third position.               |
| **pos4**     | **`vector_2d`** | Fourth position.              |
| **color**    | **`color`**     | Optional. Color of the image. |
| **rounding** | **`number`**    | Optional. Image rounding.     |

### image

`draw.image(texture: texture, x: number, y: number, width: number, height: number, color: color[, rounding: number])`

| Name         | Type          | Description               |
| ------------ | ------------- | ------------------------- |
| **texture**  | **`texture`** | Texture.                  |
| **x**        | **`number`**  | X position.               |
| **y**        | **`number`**  | y position.               |
| **width**    | **`number`**  | Width.                    |
| **height**   | **`number`**  | Height.                   |
| **color**    | **`color`**   | Color of the image.       |
| **rounding** | **`number`**  | Optional. Image rounding. |

### shadow

`draw.shadow(x: number, y: number, width: number, height: number, length: number, color: color[, x_offset: number, y_offset: number])`

| Name          | Type         | Description          |
| ------------- | ------------ | -------------------- |
| **x**         | **`number`** | X position.          |
| **y**         | **`number`** | y position.          |
| **width**     | **`number`** | Width.               |
| **height**    | **`number`** | Height.              |
| **length**    | **`number`** | Shadow length.       |
| **color**     | **`color`**  | Color of the shadow. |
| **x\_offset** | **`number`** | Optional. X offset.  |
| **y\_offset** | **`number`** | Optional. Y offset.  |

### push\_clip\_rect

`draw.push_clip_rect(x: number, y: number, width: number, height: number)`

| Name       | Type         | Description |
| ---------- | ------------ | ----------- |
| **x**      | **`number`** | X position. |
| **y**      | **`number`** | y position. |
| **width**  | **`number`** | Width.      |
| **height** | **`number`** | Height.     |

Applies the clip region to the given rectangle for all subsequent elements.

### pop\_clip\_rect

`draw.pop_clip_rect()`

Discards an early set rectangle clipping region.
