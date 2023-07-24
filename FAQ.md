What's included in MythicMobs Premium?
--------------------------------------

[MythicMobs
Premium](http://www.mythicmobs.net/index.php?account/upgrades) comes
with numerous Premium-only perks, including:

-   Special Premium role in Discord
-   Access to the premium support channel and ticket system
-   Access to the latest version faster
-   Access to development builds
-   Math and Placeholders are usable in most skills, drop amounts, and
    options
-   Ability to use hit-conditions in any projectile skills
-   Ability to use custom damage types and damage modifiers
-   Ability to use several custom AI goals/targeters that can use
    conditions

More premium-only features will continue to be added as time goes on.

You can upgrade your account to Premium [by clicking
here](http://www.mythicmobs.net/index.php?account/upgrades).

For those who wish to donate a little more or who have large servers,
our Premium+ package gives you several added benefits:

-   Special Premium+ role in Discord
-   Priority on support tickets
-   License usable on multiple servers you own

My mob disappears when I try to make a passive mob attack something!
----------------------------------------------------------

Passive mobs types (sheep, pigs, cows, Etc.) are unable to attack any entity as the base mob does not have the ability to deal damage. In older versions of Minecraft, this behaviour may crash the server, while on newer versions the mob simply vanishes. The best way to work around this is to use a hostile mob type (such as a zombie), and disguise it as a passive mob type using LibsDisguises.

How can I get custom heads on my mob?
-------------------------------------

Hold the head in your hand and use the \`mm i import\` command to import
it as a MythicItem. Set the item the same way you would any other
helmet.

How do I make "caster" mobs that cast spells instead of using melee attacks?
----------------------------------------------------------------------------

The best way to go about doing this is using a projectile casted onTimer. A more thorough example can be found on the wiki page for [Projectiles](/skills/mechanics/projectile).

How do I use color codes in Player Disguises?
---------------------------------------------

Make sure to use Disguise: option and use single quotes (‘ ‘) around the
color code.

My particles are too spread out!
--------------------------------

Set the particle skill’s hS and vS to 0.1, the flame particles are
naturally widespread as they are actually blaze and furnace particles
that play in a wide fashion.

To narrow down their particles, you need to narrow down their radiuses
both horizontally and vertically. Very small radiuses will keep them
looking like a nice straight fiery line.

Why can't I set a mob's health above 2000?
------------------------------------------

This is a problem with Spigot. Simply go into your spigot.yml config
file and increase the max-health property.

How do I create a complex multi-skilled mob that won’t use all of its skills at the same time?! Its too OP!
-----------------------------------------------------------------------------------------------------------

There are many ways of spacing out mob skills to make them less
predictable, more spread out, and more random.

-   You can use the RandomSkill skill to cast random skills on an
    interval
-   Use the "GCD" (global cooldown) skill along with the "OffGCD"
    condition.
-   Give your skills lower chances and cooldowns.
-   Uses stances via the setstance mechanic and the stance condition.

I want to use my own custom sound effect, how do I do this? (Answer provided by SeanArmor on the MythicMobs forums)
-------------------------------------------------------------------------------------------------------------------

To use custom sounds, they must be added to the resource pack your
server is using. Players that don't use a resource pack with the custom
sounds will NOT be able to hear them.

Go to [www.wowhead.com/sounds](http://www.wowhead.com/sounds) or some
other sound websites. Download the sound file. Than convert the sound
file using
[audio.online-convert.com/convert-to-ogg](http://audio.online-convert.com/convert-to-ogg)

Or using SeanArmor's method <u>(not sure if this works)</u> Rename your
file with the extension of .ogg

Then put your new .ogg sound into your resource pack folder, and use the
effect:sound{something.something.yoursoundname}

The something.something is the folder path to your file. So if your .ogg
is in just the resource pack folder you would just put the name without
the .ogg extension in the skill. If it was in a folder for Example
(FolderA/FolderB/yoursound.ogg) you would type
effect:sound{FolderA.FolderB.yoursound}