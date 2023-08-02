## 用途
復原上一個貼上的動作 [技能:fawePaste]


## 細項設定
| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|---------------------------------------------------------------|---------------|
| schematic |  s   | 要取消貼上的結構 | |
| pasteID   | pid, id  | 要取消貼上的ID  |   |

## 範例

```yml
ExampleMob:
  Skills:

  # 有 ID
  - fawePaste{s=cgym.schem;id=abc} @self ~onSpawn
  - undoPaste{id=abc} @self ~onDamaged

  # 沒 ID
  - fawePaste{s=lab.schem} @self ~onSpawn
  - undoPaste{id=lab.schem} @self ~onDamaged
```

[技能:fawePaste]: /Skills/mechanics/fawepaste/