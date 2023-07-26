Mechanic: Random Message
========================

Sends a random message to the target player. Does nothing if the target
is not a player. No limit to how much messages can be added to the list.
The special character # will cause this skill to fail.

細項設定
----------

| Attribute | Aliases | Description   | Default Value |
|-----------|---------|---------------------------------------------------------------------------------------------------------------------------------------|---------------|
| messages  | m   | A list of message strings to send to the player, separated by commas. Each string must be in quotes. These strings can use variables. |   |

  

範例
--------

  Skills:
  - randommessage{
  m=
  "message 1",
  "message 2",
  "message 3";
  } @PIR{r=20} ~onInteract

Skills:
- randommessage{m="one test","not a test","test";} @PIR{r=20} ~onInteract
