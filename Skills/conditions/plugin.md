## 用途
Checks if the specified plugin is running on the server


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| plugin| pl, p | The plugin to check for  | MythicMobs |


## 範例
```yml
  Conditions:
  - plugin{p=ThePluginName} true
```


## 簡化寫法
- [x] pluginexists
- [x] hasplugin