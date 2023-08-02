## 用途
向可設定屬性的目標添加屬性倍率器


## 細項設定

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| attribute | attr  | 要設置的屬性  | GENERIC_LUCK |
| operation | op| 要執行的操作 | ADD_NUMBER |
| amount| amt, a| 要設置的倍率 | 0 |
| duration  | dur   | 要持續多久(單位:ticks) | 0 |


## 範例
```yml
ExampleMob:
  Type: ZOMBIE
  Skills:
  - attributeModifier{attribute=GENERICK_LUCK;a=2;d=1200;op=ADD_NUMBER} @trigger ~onDeath
```