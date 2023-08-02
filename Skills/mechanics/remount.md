用途
=================

重新騎乘施法者最初騎乘的生物(如果它還活著)

範例
--------
一隻名為 "Rider" 的生物預設騎著 "TestHorse"，

當受傷時下馬，互動時若 "TestHorse" 還活著則重新騎上
```yml
Rider:
  Mobtype: skeleton
  Display: 'Rider'
  Health: 12
  Mount: TestHorse
  Skills:
  - dismount ~onDamaged
  - remount ~onInteract
TestHorse:
  Mobtype: horse
  Display: 'Test Horse'
  Health: 20
```