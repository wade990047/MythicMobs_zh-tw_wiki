## 用途
將扇形範圍內的所有實體設為目標(可指定項:角度、半徑、旋轉角度)


## 細項設定
| 設定項 | 簡寫   | 用途                      | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| angle     | a         | 扇形角度           | 90      |
| range     | r         | 扇形長度           | 16      |
| rotation  | rot       | 扇形旋轉角度        | 0       |


## 範例
```yaml
ExampleSkill:
  Skills:
  - ignite @LivingInCone{a=45;r=20}
```


## 簡化寫法
- [x] entitiesInCone
- [x] livingEntitiesInCone
- [x] LEIC
- [x] EIC