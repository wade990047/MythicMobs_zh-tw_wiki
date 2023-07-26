Mechanic: Send Resource Pack
============================

Sends a resource pack to the targeted player.

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|------------------------------------------------------|---------------|
| url   | u   | The link to the resourcepack to download.| NONE  |
| hash  | h   | The hash for the resource pack (not currently used). | mythicmobs|

  

範例
--------

*Note: the hash provided in this example is just a demonstration, do not
use it in your skill.*

  Skills:
  - sendresourcepack{url="https://yourresourcepackurlhere";hash="cf23df2207d99a74fbe169e3eba035e633b65d94"} @PIR{r=15} ~onSpawn
  - ...
