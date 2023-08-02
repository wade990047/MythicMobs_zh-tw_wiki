## 用途

強制使狼坐下

## 細項設定

| 設定項 | 簡化寫法 | 用途 | 預設值 |
| --------- | ----- | -----|------ |
| state |   | 是否坐下| |

## 範例

```yml
# 站著
- wolfSit{state=false} @self ~onInteract
```

```yml
# 坐著
- wolfSit{state=true} @self ~onInteract
```