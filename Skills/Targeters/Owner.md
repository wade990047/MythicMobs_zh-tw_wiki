## 用途
將施法者的擁有者設為目標  
擁有者可以透過技能 **[SetOwner](/Skills/mechanics/setowner)** 進行設定

## 範例
這項技能會向施法者的擁有者發送一條消息
```yaml
ExampleSkill:
  Skills:
  - message{m="Hello there!"} @Owner
```