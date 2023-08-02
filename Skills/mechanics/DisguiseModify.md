## 用途
編輯正在使用偽裝的實體.  

**技能: [Disguise](/skills/mechanics/disguise)**

**插件: [LibsDisguises](https://www.spigotmc.org/resources/libs-disguises-free.81/)** 、 
**[ProtocolLib](https://www.spigotmc.org/resources/protocollib.1997/)** 必須確實安裝

你可以在這裡找到可以變更的選項 [偽裝](/Mobs/Disguises)
所要填入的值會與指令 `/modifydisguise` 一樣


## 細項設定

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| disguise  | d, type   | 要變更的偽裝設定項 | player Ashijin |


## 範例
這項偽裝將會使手上物品拿著**"空氣"**
```yml
  Skills:
  - disguisemodify{d="setItemInMainHand air"} @self 
```

##
這項偽裝將會使手上物品拿著**"原始手上物品"**
```yml
  Skills:
  - disguisemodify{d="setItemInMainHand %held-item%"} @self
```


## 簡化寫法
- [x] modifydisguise