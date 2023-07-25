## 用途
Modifies an *already* applied disguise on the target entity.  
Like the [Disguise](/skills/mechanics/disguise) mechanic, [LibsDisguises](https://www.spigotmc.org/resources/libs-disguises-free.81/) and [ProtocolLib](https://www.spigotmc.org/resources/protocollib.1997/) must be installed. [Here](/Mobs/Disguises) you can find our documentation on the matter.  
The syntax for the disguise in this mechanic is completely equivalent to the one used in the `/modifydisguise` command.


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| disguise  | d, type   | The options to modify in the disguise | player Ashijin |


## 範例
This will set the displayed item in the disguises's main has as "air"
```yaml
  Skills:
  - disguisemodify{d="setItemInMainHand air"} @self 
```

##
This will set the item displayed in the disguise's main hand as the real one
```yaml
  Skills:
  - disguisemodify{d="setItemInMainHand %held-item%"} @self
```


## 簡化寫法
- [x] modifydisguise