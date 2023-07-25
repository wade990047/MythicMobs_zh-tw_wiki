## 用途
A condition that checks checks if the target has a velocity matching the given parameters.

If the X, Y, or Z velocity is not specified, that component of the velocity is not checked. The 'absx', 'absy', and 'absz' options determine whether the absolute value of the corresponding velocity is used in the check. If 'relative' is true, the velocities are considered relative to the entity's orientation.

## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| x  |  |  The X velocity |  NONE  |
| y  |  |  The Y velocity |  NONE  |
| z  |  |  The Z velocity |  NONE  |
| absx  |  |  Use the absolute value of the X velocity |  false  |
| absy  |  |  Use the absolute value of the Y velocity |  false  |
| absz  |  |  Use the absolute value of the Z velocity |  false  |
| relative  |  |  If true, X is forward/backward and Z is side-to-side |  false  |

## 範例

In this example, we check if the players X velocity is under an absolute value of 5.

```yaml
  Conditions:
  - directionalVelocity{x=<5;absx=true} true
```