用途
================

編輯目標對於施法者威脅表的威脅值 **(生物必須開啟威脅表)**

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|-----------------------------------------------------------|---------|
| amount| a   | 要給予目標的值(可以是負值) | 1   |
| mode  | m   | 動作: Add / Remove / Multiply / Divide / Set / Reset / Forcetop | Add |

Set/reset/forcetop 這三種動作不需要 “amount=” 的設定

範例
--------

範例中怪物會在重生時將最近的玩家設置10000點的威脅值

```yml
Fixate:
  Skills:
  - threat{amount=10000} @NearestPlayer ~onSpawn
```