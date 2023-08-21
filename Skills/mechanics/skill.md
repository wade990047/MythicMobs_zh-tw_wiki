用途
===============

呼叫其他已經完成的技能組

技能必須要存在於 **`/MythicMobs/Skills`**

技能內若沒有指定目標，則將自動引用最外層所指定的目標

寫法
------
```yml
  Skills:
  - skill{skill=AnotherSkill} @Target ~onAttack
  - skill{s=AnotherSkill} @Trigger ~onSpawn
  - skill:OtherSkill @Trigger ~onDeath
```
---
設定項 **`sync=true`** 會被強制繼承到技能組內所有技能，不可於後續執行時關閉

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|-----------|---------------------------------|---------|
| skill | s | 要被執行的技能組  | |
| forcesync | sync  | 是否強制該技能與Minecraft同步執行 | false   |

冷卻
--------

你可以為你的技能添加冷卻，方式如下

```yml
自訂的技能名稱:
  Cooldown: <seconds> #單位: 秒
  Conditions: #條件式
  - condition
  - ...
  Skills: #要執行的技能
  - mechanic{}
  - ...

```
這只適用於儲存在 **`/MythicMobs/Skills`** 中的技能檔案

---
冷卻技能
---------------

當主要技能正在冷卻時，允許直接執行其他技能

```yml
自訂的技能名稱:
  Cooldown: <seconds>
  OnCooldownSkill: 自訂的冷卻讀取技能名稱 #冷卻時要執行的技能
  Skills:
  - mechanic{}
  - ...

自訂的冷卻讀取技能名稱: #需和上方 OnCooldownSkill 的名稱相同
  Skills:
  - mechanic{}
  - ...
```

**筆記：** 設置為 OnCooldownSkill 的技能本身也可以有一個 OnCooldownSkill 的設定。

範例
--------

```yml
  Skills:
  - skill{s=AnotherSkill;sync=true} @Target ~onAttack
  - skill{s=ice_bolt;sync=true} @Target ~onTimer:100
  - skill{sync=true;s=flamethrower} @TargetLocation ~onTimer:200
  - skill:Onemechainc @Target ~onDamaged
  - skill
  {
  skill=leafs;
  sync=true
  }
```