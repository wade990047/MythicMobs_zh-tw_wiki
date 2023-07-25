## Targeter: Rectangle
將組成矩形的目標位置點設為目標

根據參數，可以修改矩形的某些元素，例如是否填充或不填充，是否僅針對其輪廓、位置等

### 細項設定

| 設定項  | 簡寫  | 用途| 預設值 |
|----------------|----------|------------------------------------------------------------|:-------:|
| x  |  | **x** 軸上矩形的大小| |
| y  |  | **y** 軸上矩形的大小| |
| z  |  | **z** 軸上矩形的大小| |
| xOffset|  | 矩形在 **x** 軸上的偏移量  | |
| yOffset|  | 矩形在 **x** 軸上的偏移量  | |
| zOffset|  | 矩形在 **z** 軸上的偏移量  | |
| points | p| 每個立方體`線`的數量   | |
| filled | fill, f  | 矩形應該被填充 | |
| outline| edge, onlyEdge, e, onlyOutline, o | 只畫輪廓 |   |
| rotation   | r| 矩形的 3D 旋轉   | |
| fromOrigin | origin   | 矩形是否應該從技能的起點繪製 |  |

## 範例
```yaml
ExampleMob1:
  Type: ZOMBIE
  Skills:
  - e:p{p=FLAME;a=1} @Rectangle{d=12;f=false;r=45,45,0;yOffset=1.5;outline=true} ~onDamaged

ExampleMob2:
  Type: ZOMBIE
  Skills:
  - e:p{p=SOUL_FIRE_FLAME;a=1} @Rectangle{d=12;r=45,45,45;yOffset=3;fill=true} ~onDamaged
```