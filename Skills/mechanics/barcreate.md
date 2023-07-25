Mechanic: Bar Create
====================

在施法生物上創建一個自定義BOSS血條(不能是玩家)

細項設定
----------

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|---------|---------------------------------------------------------------------------------------------------------------------|-----------------------------|
| name  | n   | BOSS血條名稱 | infobar |
| display   | d   | BOSS血條顯示內容| &lt;skill.var.aura-name&gt; |
| value | v   | BOSS血條的填充量，必須是 0.0 到 1.0 之間   | 1.0 |
| color | c   | BOSS血條的顏色. 允許的值有: PINK, BLUE, RED, GREEN, YELLOW, PURPLE, WHITE | RED |
| style | s   | BOSS血條的類型. 允許的值有: SOLID, SEGMENTED_6, SEGMENTED_10, SEGMENTED_12, SEGMENTED_20  | SOLID   |

範例
--------

  Skills:
  - barCreate{name="MyBossBar";display="<caster.name> - <caster.hp>";value=1.0;color=BLUE;style=SEGMENTED_6} @self ~onSpawn
  - ...