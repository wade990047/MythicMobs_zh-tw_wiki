Mechanic: RandomSkill
=====================

Executes a random skill from the list of supplied
[skills](skills/mechanics/skill). Will ignore any skills that are on
cooldown. There is no limit to how much skills can be added.

細項設定
----------

| 設定項 | 簡化寫法 | 用途  | 預設值 |
|-----------|---------|---------------------------------------------------------|---------|
| skills| | The list of skills to execute, must be separated by a `,` | |
| fallbackskill | fbskill, fbs | the metaskill to run if condition checks fail for all skills in the randomskill list |



範例
--------

Skills:
- randomskill{skills=skill1,skill2,skill3}

Having problems overviewing your randomskill-syntax? Try this:

Skills:
- randomskill{
skills=
superskill,
green_skill,
skill3,
grandSkill,
7331
}

You can also make your skills be executed with different chances via the weight system. Skills without a weight will default to weight 1.

Skills:
- randomskill{skills=metaskill 10,otherskill 0.5,someskill 0,testskill}