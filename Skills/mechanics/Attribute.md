## 用途
設置目標實體的屬性


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| attribute | attr  | 要設置的屬性   | GENERIC_LUCK |
| amount| amt, a| 要設置的值 | 0 |
| duration  | dur   | 要持續多久(單位:ticks) | 0 |


## 範例
```yaml
ExampleMob:
  Type: ZOMBIE
  Skills:
  - attribute{attribute=GENERICK_LUCK;a=2;d=1200} @trigger ~onDeath
```


## 簡化寫法
- [x] setattribute