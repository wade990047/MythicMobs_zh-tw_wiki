## 用途
將定位原點周圍指定環型中的位置設為目標

## 細項設定
| 設定項 | 簡寫   | 用途                      | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| radius    | r         | 目標半徑範圍       | 5       |
| points    | p         | 組成環形的點數量 | 10      |
| rotationx | rotx, rx  | 環型在 **x** 軸上的旋轉角度                            | 0       |
| rotationy | roty, ry  | 環型在 **y** 軸上的旋轉角度                                | 0       |
| rotationz | rotz, rz  | 環型在 **z** 軸上的旋轉角度                             | 0       |
| offsetx   | offx, ox  | 環型在 **x** 軸上的偏移                                 | 0       |
| offsety   | offy, oy  | 環型在 **y** 軸上的偏移                                 | 0       |
| offsetz   | offz, oz  | 環型在 **z** 軸上的偏移                                 | 0       |

## 範例
```yaml
ExampleSkill:
  Skills:
  - projectile{...;
    onEnd=[
      - effect:particles @RingAroundOrigin{r=5;p=15}
    ]}
```


## 簡化寫法
- [x] ringOrigin
- [x] RAO