# ✨ beam\_sys

### draw\_beam\_circle\_points

`beam_sys.get_material_by_name(beam_info: beam_info)`

### draw\_beam\_points

`beam_sys.draw_beam_points(beam_info: beam_info)`

### draw\_beam\_ring

`beam_sys.draw_beam_ring(beam_info: beam_info)`

### draw\_beam\_ring\_point

`beam_sys.draw_beam_ring_point(beam_info: beam_info)`

| Name            | Type    | Description |
| --------------- | ------- | ----------- |
| m\_vecStart     | vector  | -           |
| m\_vecEnd       | vector  | -           |
| m\_nType        | integer | -           |
| m\_bRenderable  | bool    | -           |
| m\_nFlags       | integer | -           |
| m\_pszModelName | string  | -           |
| m\_flHaloScale  | float   | -           |
| m\_flLife       | float   | -           |
| m\_flWidth      | float   | -           |
| m\_flEndWidth   | float   | -           |
| m\_flFadeLength | float   | -           |
| m\_flAmplitude  | float   | -           |
| m\_flSpeed      | float   | -           |
| m\_flFrameRate  | float   | -           |
| m\_nHaloIndex   | integer | -           |
| m\_nStartFrame  | integer | -           |
| m\_flBrightness | float   | -           |
| m\_flRed        | float   | -           |
| m\_flGreen      | float   | -           |
| m\_flBlue       | float   | -           |

### using:

```lua
local beam = beam_info()
beam.m_flRed = 15
beam.m_flGreen = 15
beam.m_flBlue = 16
```
