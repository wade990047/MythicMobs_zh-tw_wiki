## 用途
將施法者周圍球體中的點設為目標


## 細項設定
| 設定項 | 簡寫   | 用途                      | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| radius    | r         | 目標半徑範圍       | 5       |
| points    | p         | 目標點的數量             | 10      |
| yoffset   | y         | 目標在 y 軸上的偏移                              | 0       |

## 範例
```yaml
ExampleSkill:
  Skills:
  - effect:particles @Sphere{r=6;points=50}
```