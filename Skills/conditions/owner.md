## 用途
Checks if the target entity is the owner of the caster. 

- If the caster is a tamable mob, if will check if the target entity is the mob's "vanilla" owner
- If the caster is not a tamable mob, then to match the target entity must have been set as the owner via the [SetOwner](/skills/mechanics/setowner) mechanic


## 細項設定
> *This condition has no attributes*


## 範例:
```yaml
  TargetConditions:
  - owner{} true
```