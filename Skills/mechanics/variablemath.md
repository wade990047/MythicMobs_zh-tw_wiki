用途
======================

將變量設置為一元一次方程式的答案，其中`x`是 [變量](/skills/variables) 的當前值。

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|---------------|---------------|
| var   | | 變量名稱  |   |
| equation  | eq, e   | 算式，必須用雙引號(")包圍 |   |

  
範例
----

將一個變數儲存至佔位符內
```yml
MMOVar:
  Skills:
  - variableMath{var=target.exp;equation="%mmocore_level%"}
```
---
進行數學運算
```yml
Math1:
  Skills:
  - variableMath{var=caster.damage;equation="<caster.hp>*5"}
Math2:
  Skills:
  - variableMath{var=caster.speed;equation="(<caster.var.age>/5)+1"}
```