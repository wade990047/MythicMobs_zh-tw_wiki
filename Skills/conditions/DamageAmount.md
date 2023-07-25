## 用途
Checks for a range of damage the entity took, if the skilltree originated from a [onDamaged Trigger](/Skills/Triggers#ondamaged) or an [onDamaged Aura](/skills/mechanics/ondamaged).


## 細項設定

| Attribute | Aliases  | Description  | Default |
|-----------|--------------|-------------------------------------------------------------------|---------|
| damageAmount | amount, a | Range of damage to check for | >0  |


## 範例
```yaml
  Conditions:
  - damageamount{amount=>10} true
```