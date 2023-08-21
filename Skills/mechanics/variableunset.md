用途
=======================

刪除指定 [變量](/skills/variables)

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|------------|---------------|
| variable  | var | 變量名稱，可以通過 **scope.** 來補足設定項  |   |
| scope | s   | 變量的 [所屬位置](/skills/variables#variable_scopes) | SKILL |


技能新增於MM版本 v4.12

 
範例
----

刪除施法者在`caster`位置底下的`testing`變量

```yml
RemoveVariable:
  Skills:
  - variableUnset{var=caster.testing} @self
```
結果同上
```yml
RemoveVariable:
  Skills:
  - variableUnset{var=testing;scope=caster} @self
```