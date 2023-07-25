## 用途
Tests if the target is **not** within the given angle from where the caster is looking.


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| angle | a | The angle of the FOV to check in| 90  |
| rotation  | r | Rotates the FOV to check in | 0   |


## 範例
```yaml
  TargetConditions:
  - fieldofview{angle=90} true
```
This condition will filter out every target that is within a 90 degree field of view of the caster.

##
```yaml
  TargetConditions:
  - fieldofview{angle=90} false
```
This condition will allow to be targeted only entities that are within a 90 degree field of view of the caster.


## 簡化寫法
- [x] infieldofview
- [x] fov