## 用途
讓目標執行指令.

顏色代碼與變量都被允許使用 

顏色代碼查看 [所有顏色代碼](/databases/misc/colorcodes)

變量查看 [所有文字變量](/skills/stringvariables)

指令技能不會自訂修復有問題的地方，所以像是"或是{}必須要用佔位符來取代

否則會造成技能的錯誤 

特殊字元列表 [特殊字元佔位符](/skills/Placeholders#special-characters)


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| command   | c, cmd| 要執行的指令  | |
| asCaster  | ac, caster, sudo, asmob| 是否由施法者執行指令，若否則由控制台執行 | false   |
| asOp  | op| 是否執行時以op權限執行  | false   |
| asTarget  | at, target, sudotarget| 是否由目標執行指令，若否則由控制台執行  |  false  |
| requireTarget | rt| 技能擊中特定目標時才執行指令  | asTarget's value|

  

## 範例

### 正確的指令技能寫法
```yaml
  Skills:
  - command{c="give <target.name> gold_ingot 20"} @trigger ~onInteract
  - command{c="minecraft:tp <target.name> <mob.uuid>"} @self ~onDamaged
  - command{c="minecraft:summon Zombie ~ ~ ~ <&lc>NoAI:true,CustomName:<&dq>Summoned Zombie<&dq><&rc>"}
  - command{c="minecraft:summon Zombie ~ ~ ~ {NoAI:true,CustomName:<&dq>Summoned Zombie<&dq>}"}
  - command{c="say HELLO <target.name>";asTarget=true;asOp=true} @NearestPlayer{r=10}
```

### 錯誤的指令技能寫法

下方的技能將不會執行，並且有可能造成技能組錯誤

"或是{}必須要用佔位符來取代

特殊字元列表 [特殊字元佔位符](/skills/Placeholders#special-characters)
```yaml
  Skills:
  - command{c="minecraft:summon Zombie ~ ~ ~ {NoAI:true,CustomName:"Summoned Zombie"}"}
```

##

### **讓玩家執行一條技能**
下方的範例會讓與怪物進行互動的玩家執行 say 的指令
```yaml
ExampleMob:
  Type: ZOMBIE
  Skills:
  - command{c="say <target.name>";asTarget=true;asOp=true} @trigger ~onInteract
```

教學
---------

-   [村民交易配合指令技能 製作者: Krowerom](https://www.youtube.com/watch?v=p71bl_W3a4I&feature=youtu.be)