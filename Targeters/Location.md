## 用途
將世界的指定坐標設為目標


## 細項設定
| 設定項 | 簡寫   | 用途                      | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| location  | loc, l, c | 完整的資料型態, 格式為 `x,y,z,yaw,pitch`                  |         |
| x         |           | 如果 `location` 沒有被設定, 這項用來設定 **x** 座標 | 0     |
| y         |           | 如果 `location` 沒有被設定, 這項用來設定 **y** 座標 | 0     |
| z         |           | 如果 `location` 沒有被設定, 這項用來設定 **z** 座標 | 0     |
| yaw       |           | 如果 `location` 沒有被設定, 這項用來設定頭的前後左右偏移       | 0      |
| pitch     |           | 如果 `location` 沒有被設定, 這項用來設定頭的上下偏移       | 0      |


## 範例
```yaml
ExampleSkill:
  Skills:
  - setblock{m=DIAMOND_BLOCK} @Location{location=100,70,-120,0,0}
  - setblock{m=EMERALD_BLOCK} @Location{x=100;y=71;z=-120}
```