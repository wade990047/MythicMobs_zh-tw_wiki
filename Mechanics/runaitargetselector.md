用途
=============================

**設定項**: aitarget

執行目標的 AITargetSelectors

[可用的AI攻擊目標](/Mobs/Custom-AI#ai-target-selectors)

範例
-------
```yml
ChangePatchfinderGoalExample:
  Skills:
  - runaitargetselector{target=clear}
  - runaitargetselector{target=players}
  - runaitargetselector{target=monsters}
```