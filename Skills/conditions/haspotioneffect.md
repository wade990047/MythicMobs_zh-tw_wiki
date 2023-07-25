## 用途
Tests if the target entity has a potion effect


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| type  | t | The potion effect type  | ANY |
| level | lvl, l| An optional level range to match| |
| duration  | d | An optional duration range to match | |


## 範例
```yaml
  Conditions:
  - haspotioneffect{t=SLOW;l=0-2;d=0-9999} true
```

```yaml
  TargetConditions:
  - haspotioneffect{t=Speed;l=0-9} true
```


## 簡化寫法
- [x] hasPotion