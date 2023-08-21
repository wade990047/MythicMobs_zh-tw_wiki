用途
====================

以怪物的傷害為基礎，造成指定倍率的傷害

細項設定
----------

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|------------------|---------|-------------------------------------|---------|
| multiplier   | m   | 傷害倍率| 1   |
| ignoreArmor  | ia  | 是否無視盔甲  | false   |
| preventknockback | pkb, pk |是否無視攻擊擊退 | false   |
| preventimmunity  | pi  | 是否無視受傷冷卻 | false   |

  

範例
--------
怪物將會在受到傷害時造成目標
10 * 1.5 的傷害
即 15 點傷害
```yaml
AMob:
  Type: HUSK
  Damage: 10
  Skills:
  - basedamage{m=1.5} @target ~onDamaged
```
[1] 1 = 100%, 0.5 = 50% 以此類推