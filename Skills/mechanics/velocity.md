用途
==================

編輯目標實體的重力

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|-------------------------------------------------------------------------|---------------|
| mode  | m   | 變更的類型. 可以是 SET, ADD, REMOVE, DIVIDE, MULTIPLY. | SET   |
| velocityx | vx, x   | 對於 x 軸的重力.   | 1 |
| velocityy | vy, y   | 對於 y 軸的重力.   | 1 |
| velocityz | vz, z   | 對於 z 軸的重力.   | 1 |
| relative  | | 速度的變化是否應該相對於施法者面對的方向。在這種情況下，"x"軸變為"前/後"，"y"變為"上/下"，"z"變為"左/右"| false |

  

範例
--------

停止施法生物的所有重力移動。該效果持續到生物再次移動或被其他來源移動。

```yml
internal_mobname:
  Type: Zombie
  Skills:
  - velocity{m=set;x=0;y=0;z=0} @self ~onDamaged
```

雖然上面的示例在大多數情況下都有效，但弓的擊退附魔仍然可以移動。
<br>可以通過對技能進行輕微修改來防止這種情況，如下所示。

```yml
internal_mobname:
  Type: Zombie
  Skills:
  - velocity{m=set;x=0;y=0;z=0;delay=1} @self ~onDamaged
```