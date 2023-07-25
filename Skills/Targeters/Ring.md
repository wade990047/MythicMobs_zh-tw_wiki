## 用途
用點形成環型，將每點位置設為目標

## 細項設定
| 設定項 | 簡寫   | 用途  | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| radius| r | 目標半徑範圍   | 5   |
| points| p | 組成環型的點數量 | 10  |
| rotationx | rotx, rx  | 環在 **x** 軸上的旋轉  | 0   |
| rotationy | roty, ry  | 環在 **y** 軸上的旋轉  | 0   |
| rotationz | rotz, rz  | 環在 **z** 軸上的旋轉   | 0   |
| offsetx   | offx, ox  | 環在 **x** 軸上的偏移   | 0   |
| offsety   | offy, oy  | 環在 **y** 軸上的偏移 | 0   |
| offsetz   | offz, oz  | 環在 **z** 軸上的偏移 | 0   |

## 範例
```yaml
ExampleSkill:
  Skills:
  - effect:particles @Ring{r=10;p=15}
```