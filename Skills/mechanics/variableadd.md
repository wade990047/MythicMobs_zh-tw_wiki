用途
---

將指定 [變量](/skills/variables) 添加數值，只適用於整數與浮點數類型

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|------------------------------------|---------------|
| var   | name, key |  變量名稱 | None |
| amount| a   | 變更數值 | 1 |

  

範例
--------
```yml
  Skills:
  - variableadd{var=skill.testVar;amount=1} ~onInteract
  - ...
```