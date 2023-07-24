## Description
Targets locations in a specified ring around the caster

## Attributes
| Attribute | Aliases   | Description                                                          | Default |
|-----------|-----------|----------------------------------------------------------------------|---------|
| radius    | r         | The radius of the targeter                                           | 5       |
| points    | p         | The points that make up the ring                                     | 10      |
| rotationx | rotx, rx  | The rotation of the ring on the x axis                               | 0       |
| rotationy | roty, ry  | The rotation of the ring on the y axis                               | 0       |
| rotationz | rotz, rz  | The rotation of the ring on the z axis                               | 0       |
| offsetx   | offx, ox  | The offset of the ring on the x axis                                 | 0       |
| offsety   | offy, oy  | The offset of the ring on the y axis                                 | 0       |
| offsetz   | offz, oz  | The offset of the ring on the z axis                                 | 0       |

## Examples
```yaml
ExampleSkill:
  Skills:
  - effect:particles @Ring{r=10;p=15}
```