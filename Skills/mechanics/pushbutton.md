Mechanic: Push Button
---------------------

Pushes a button at the supplied coordinates.

細項設定
----------

| Attribute | Aliases| Description   | Default Value |
|-----------|--------|--------------------------------------------|---------------|
| x || The X coordinate of the button.| 0 |
| y || The Y coordinate of the button.| 0 |
| z || The Z coordinate of the button.| 0 |

  

範例
--------
```yaml
HitSecretButton:
  Skills:
  - pushbutton{x=15;y=67;z=-213}
```