## 用途
將主技能起點指定半徑內的所有方塊設為目標


## 細項設定
| 設定項 | 簡寫   | 用途                      | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| radius    | r         | 目標半徑範圍       | 2       |
| radiusy   | ry, yradius, yr |  y 的半徑                                  | radius  |
| shape     | s         | 所選涵蓋方塊的形狀。可以示 `SPHERE`, `CUBE`            | SPHERE  |
| noise     | n         | 目標的隨機性   | 0       |
| noair     | na        | 是否不應將空氣作為目標                                   | true    |
| onlyair   | oa        | 是否只針對空氣                                  | false   |


## 範例
技能將針對技能起點周圍半徑 10 格內的一些方塊

```yaml
ExampleSkill:
  Skills:
  - effect:particles @BlocksNearOrigin{r=10;noise=0.5}
```


## 簡化寫法
- [x] BNO