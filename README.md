# granadoespadav32setup
granadoespadav32 private server setup
Granado Espada v32.18.19 retail server files

MY DISCORD IF YOU NEED HELP - Abysmal#0666

ORIGINAL Video Showcasing the server files - https://www.youtube.com/watch?v=VHzrp2-Nfyc
DISCORD GROUP - https://discord.gg/DbxUSpn6kD

To start off this guide I want you to know anything is possible including building your own server with these files!
if you need any help come join the v32 developer discord everyone can help eachother there and will have new guides and stuff regularly!
DEVELOPER Discord LINK - https://discord.gg/zeYzb6kc

** DOWNLOADS **
microsoft sql (if you dont have it yet) - https://www.microsoft.com/en-us/download/details.aspx?id=8109 
GE_Server ge and release folder - https://drive.google.com/file/d/1rY9p5YS1Z2pOHdmgU49CmcZCWbETdIho/view?usp=sharing
GE V32 SQL backup - https://drive.google.com/file/d/13h4dJpu8Lu7yKlxs7UNBi6Ps8R14OzeN/view?usp=sharing
Memory cleaner if your on 32 gb ram machine - https://www.koshyjohn.com/software/memclean/

*UPDATE DOWNLOADS *
 LAVAL AND DRAKEN UPDATE FIRST - https://drive.google.com/file/d/1lArcS7b1t_ydW1FHYj2PlVnyWylAAkZy/view?usp=sharing
 ----
MERIEL UPDATE SCRIPT AND DATATABLES ONLY - https://drive.google.com/file/d/1UHUdwEJ2AMSjfXS0M9KCaiWTAaaCm2PK/view?usp=share_link
------ 
TERRA GE CLIENT MERIEL UPDATE 5/8/23 - https://drive.google.com/file/d/1VvuwthQQ7OBJbJXnWFryToAQgwTVr1mC/view?usp=sharing


*HARDWARE REQUIREMENTS*
*Minimum* - 8 core cpu Ryzen 7 5000series or better with around 4 ghz clock speed or higher is better.
32 gb ram 3200mhz is minimum you should try and run this on!
GPU is not required but reccomended any gtx 1xxx - rtx 4xxx series i recomend for smooth workflow .
*Reccomended* CPU is 16 core / 32 thread ryzen 5950x or better .
ram - reccomended should be 64 gb -128gb ram for smooth operations.



	(*Instructions*) 
First thing update your windows language settings for the release folder to function right 
in language and region settings change the "regional format" setting language to Chinese Simplified! 
(if you forget the step above the release files will not open)

*NEXT* after step above 
Build server v32 *
restore database in microsoftSQL/Navicat whatever your preference for database management.
IF YOU USING V28 FILES YOU WILL HAVE TO DELETE THIS DATABASE FIRST !
Next Right click databases and restore each bak file manually (make sure its one .bak file at a time)
go to resource and tables and change machine to 127.0.0.1 and remove 2-6 keep the 192.168.10.10
next extract files to
ge and release folders go in c:/ge_server
name folder ge_server or wont work
-----
start server v32 *
chinese name version shortcuts of node and hub + working manager client= (tools)
connect with private ge_client andromida/hell_ge/newera/terra - official client doesnt work. 
extract all ipf files (ies/xml/shared/dictionary) from client and copy them into your servers ge folder 
and make a backup before you do that .

-------------------

*EASY SETUP*
IF YOU ARE NOT INTERESTED IN EXTRACTING THE FILES AND EDITING THEM MANUALLY 
YOU CAN DOWNLOAD THE TERRA GE FILES ABOVE IN THE UPDATE DOWNLOADS .
THEN JUST EXTRACT AND REPLACE THEM ORIGINAL SERVER GE FOLDER AND DOWNLOAD THE MAY 8TH 2023 CLIENT IVE SHARED TO START PLAYING LOCALLY.

YOU CAN FIND A VIDEO GUIDE HERE! - https://www.youtube.com/watch?v=X8u8r2gNzSM

------------------------------

-------------------
*adding characters * (IF DONT WANT TO ADD MANUALLY CHECK THE NEXT GUIDE EASY SETUP) -- 

YOU will need ge_tools and the mkpatch for this part this guide is not 100% finished will be updated in more thorough explaination in v32 dev discord! 
I suggest you join!
----------------------
(First )
extract the chars your want from other ge clients including official/korean or private 
then - below*
you need to import datatable_   job / skill / stance / stancecon 
and link all those to dictionary /dictionary local if not already .
datatable_item_etc for char card 
add the character card here
and then go to editing buffs for last portion

open C: ge_server\ge\xml_export

**editing buffs **
go into folder ge_server/ge/script
you need to edit script like common_monster with in script/monster
  personal buffs @ script/buff in buff.scp
  I haven't had time to finish this guide busy releasing this guide and files etc.
  
all important datatables files under name such as 
datatable_     --- within the xml_export


** Delete Items from inventory in DB ** 
Go Navicat/MSQL 
into GE_DATA - dbo - tables - ITEM 
Filter / select CLASSID and type in class id from
DATATABLE_ITEM - WHICH EVER TABLE IT IS FROM IN XML_EXPORT

If in need of anymore guide please join our v32 developer discord for regular updates on this topic and to share your knowledge <3 !
Discord LINK - https://discord.gg/zeYzb6kc
-----------------------------------------
*EDIT GM COMMANDS*

WITHIN THE FOLDER  
C: ge_server\ge\xml_export\
edit - datatable_cheatlist.xml
----------------------------------------------

--------------------------

	*ADDING STANCE(s)*
	Update these files 
	datatable_stance / datatable_stancecondition 
	datatable_skill /datatable_buff 
	-------------- 	--------	--------	-------------	-----  dictionary_local for descriptions 
		if buffs program in func in buff.scp and/or common_monster.scp/ common_pc.scp / extraskill.scp 

---------------------
*HOW TO ADD WEAPON TO CUSTOM CHAR* / CHANGE 

Characters have specific bone annotations on them
some characters have additional annotations to support specific weapons like kess with Heavy Rifle
If you want to make Heavy Rifle appear in a character that doesnt natively support the weapon type
then look into datatable_item_weapon.xml
then for all HeavyRifle type weapons, go on the R_DUMMY column and replace bip01 prop1 with DUMMY_R_HAND_RIFLE

This will make the weapon appear for every character that supports the DUMMY_R_HAND_RIFLE
you can also opt to change it to R_HAND but it will appear in the wrong angle and will look funny lol

-----------------------------------------

--------------------------------------------------------------------

** Extra Guides **
   ------------    
** GM Commands **
ALT + f11 Item Creation Wizard Calls the item list containing most of the items in the game.
ALT + f12 Cheat List Invokes the cheat list window containing most of the GM commands. 

//gmorder
//die on (off) Invincible status
//hide on (off) Invisible to PC
//safe on (off) Cannot be attacked by monsters or PC
//tozone (all) Notice to Zone.
//Reject on (off) disable invites
//Whisper on (off) enable whispers
//expup executing command will grant experience. //expup 9999999999999
//stanceexpup executing command will grant stance experience only. //stanceexpup 9999999999999
//hpup restores HP //hpup 99999
//spup restores SP //spup 99999
//hs Changes movement speed limit of character. //hs 999
----------------------------
//toall notice to all zones
//tozone notifies the corresponding zone
//addnotice number add notice
//shownotice show notice
//mon number Enter the monster summon number to summon the specified monster "//mon number level number of objects
e.x) //mon 281 10 100
monster number 281
I summon 100 animals at level 10."
//killnpc Handle number monster disappears (without item drop) ! Kill monster with handle number confirmed by ShowState
//item number quantity item creation Creates the item according to the input quantity "//item 238 5000
Create 5000 item number 238."
//mz zone id coordinates Move the zone & connect to the start coordinates when moving coordinates specified in other zones are not entered. 
//mz reb_basic
//gocom go to family //callcom Staris
//callcom summon family to map //callcom Staris
//kickcom disconect family
//lobby create lobby from [datatable_missionpreset.xml]
//chatstop mutes a user //chatstop familyname 3000 (1 hour)
//chatstoptime stops a user's mute
//ping connection from server to pc
//w total number of players
//z check the number of players in zone (offer only?)
/navcam on(off) camera hack





--------------------------
NPC Creation tutorial:
Things needed
+ NPC you want to create
+ NPC's purpose/script
+ NPC's class_type in datatable_NPC

1. Create script somewhere in src/script/whateverfoldername
This is to keep yourself organized. I put all of my custom scripts into my own folder inside scripts, it doesn't even need to be about npc. could be mission item scripts etc. They all don't have to be in their respective folders.

2. Copy my script.
https://i.imgur.com/NEpJy1x.png
You can replace whatever you want.

3. Place NPC in a map you want.
The NPC can be in reb_basic. To see where you want the npc to be do /where and copy the coordinates onto the xml.
npcgen_reb_basic.xml

Script="NPC_TEST_SCRIPT"
ClassType="arm_judith_black" (or any npc you'd like.)

4. Done!
---------
Setup global connectivity from home connection 
use Wan IP  on only Server1_IP

In SSMS, you will need to configure the zoneserver to your IP, 
this can quickly be done by expanding the RESOURCE DB's tables and right clicking dbo.MACHINE and editing top 200 lines. 
Change the IP for the ZONE@MACHINE1 (second line) to either your LAN ip if you're running the server only for LAN, or to your WAN ip,
 if you wish the server to be public. (Note: You can skip this step if you plan to run the client on the same machine as the server, 
 but you will not be able to connect from any other computer.)

-------
zone infos 
-------------
mssms sql db 
go to resource / tables / zone_daemon - zone_master 
-------------
things to fix - and tips for gm/owner 
fix all quests  / xml must translate korean texts to english
Item folder = bless/artifact/ring/enchant/reinforce=enhance
change server rates - from GE manager client Param
skip quests - Delete stamps conditions everythere commander.(filename)

** Delete Items from inventory in DB ** 
Go Navicat/MSQL 
into GE_DATA - dbo - tables - ITEM 
Filter / select CLASSID and type in class id from
DATATABLE_ITEM - WHICH EVER TABLE IT IS FROM IN XML_EXPORT

--------------------
*DAEMON-ZONE GUIDE* UNFINISHED*
--------------------
located in SQL Databases folder - Resource - Tables - dbo.ZONE_DAEMON
102 - idk still -- btl_cas03 / dun_arm01_cash / dun_sed04
103 - ustiur -- ust_basic / btl_ust02-04 / btl_rafflesia/ btl_prison02 and _02 
104 - jaquin -- dun_jaq01 / dun_jaq_co1 / dun_jaq05 / dun_jaq03 /dun_jaq_co4 / dun_jaq06 / fld_jaq/ btl_jaq06 
105 - al que moretza /dr torsche zones -- dun_alq01 - dun_alq05 / dun_tor01 / dun_tor02 / dun_tor04 / dun_tor01_lavid / fld_tor / dun_tor_dr 
106 - coimbra - dun_ttr01/02/03/06 /-/ dun_ptv01-02-03-06 /-/ btl_ptv02 
107 - katovic  - dun_ktv01-05 / btl_ktv01-05 / btl_ktv05_tomb / dun_ktv_boss/ dun_ktv_boss 
108 - auch - auch_basic / btl_alq02 / btl_tbk01-03 / dun_tbk01-02 / dun_sil01-02 / dun_sil_boss
109 - idk - test_zone / gm_zone / event_zone / btl_ttr02 / dun_sed04 / btl_factious01
203 -   




501 - jaquin -- btl_jaq03 / btl_jaq04 / btl_jaq02 / btl_jaq01 / btl_prison01 





-


**********
Build Custom IES 
How to build native zipdecrypt:

*Install Python
*Go to -> "start" and type "Manage App Execution Aliases" .Go to it and turn off "python"
*Instal VS C++ Community Edition
*shift+right-click on empty space in tools/lib/zipdecrypt to open shell (make sure no icons are selected), there will be an option to run command prompt or powershell, either one works
*To build native _zipdecrypt module, type the ff. in cmd or powershell like so: python setup.py build_ext and copy the generated result back to tools/lib where other pyd files are located, only the pyd files are needed to be copied over

You can then start running mkpatch.cmd

first, check ⁠build-ies and do everything there until you managed to run mkpatch.cmd. you know it is successful when the last line shows the amount of time it took to run.

next, you mentioned copying of the rGE_server/release folder. i did that and one more step. you wanna check out rGE_server/ge, and you will notice the following files

1) dictionary.ipf
2) ies.ipf
3) shared.ipf
4) updateXXXXX.ipf (xxxxx is the patch number, starts with 00000 and increases by one each time you run mkpatch.cmd)

the above files can be easily seen if you sort the list of files in the folder by date modified. it will be clear on what was updated.

i made sure the game was closed (you don't have to close the server, just the client) and copied these four files over to rGE Granado Espada/ge and replaced the three existing files there.
***************************




important folders if your looking for something
---------------------
* script/system 
* xml_export -missions/reward chest /char cards ***



-----------*****





--------------------------------------------------------------------
** Extra Guides **
   ------------    
** GM Commands **
ALT + f11 Item Creation Wizard Calls the item list containing most of the items in the game.
ALT + f12 Cheat List Invokes the cheat list window containing most of the GM commands. 

//gmorder
//die on (off) Invincible status
//hide on (off) Invisible to PC
//safe on (off) Cannot be attacked by monsters or PC
//tozone (all) Notice to Zone.
//Reject on (off) disable invites
//Whisper on (off) enable whispers
//expup executing command will grant experience. //expup 9999999999999
//stanceexpup executing command will grant stance experience only. //stanceexpup 9999999999999
//hpup restores HP //hpup 99999
//spup restores SP //spup 99999
//hs Changes movement speed limit of character. //hs 999
----------------------------
//toall notice to all zones
//tozone notifies the corresponding zone
//addnotice number add notice
//shownotice show notice
//mon number Enter the monster summon number to summon the specified monster "//mon number level number of objects
e.x) //mon 281 10 100
monster number 281
I summon 100 animals at level 10."
//killnpc Handle number monster disappears (without item drop) ! Kill monster with handle number confirmed by ShowState
//item number quantity item creation Creates the item according to the input quantity "//item 238 5000
Create 5000 item number 238."
//mz zone id coordinates Move the zone & connect to the start coordinates when moving coordinates specified in other zones are not entered. 
//mz reb_basic
//gocom go to family //callcom Staris
//callcom summon family to map //callcom Staris
//kickcom disconect family
//lobby create lobby from [datatable_missionpreset.xml]
//chatstop mutes a user //chatstop familyname 3000 (1 hour)
//chatstoptime stops a user's mute
//ping connection from server to pc
//w total number of players
//z check the number of players in zone (offer only?)
/navcam on(off) camera hack

  --------------
**ADVANCE QUESTS**
  --------------
//changeproperty Quest_ID stage

//lobby create lobby from 

  --------------
**ADVANCE QUESTS**
  --------------
 * THIS GUIDE IS UNFINISHED *
//item 25276 1
quest completion speed guide 
do Scenario in order properly to avoid quest bugging
rebo - coimbra - auch 
holy water chamber 
catherine quests 
5 elements
then ustiur all the way 
then bahama scenario 1 
then errac scenario 1
then viron 
then kielce 
 and prurio
armonia  and so forth 

quest monster speed run
//mon 10631 10 20
coimbra *
phobitan -- 10341
//mon 10341 10 20

winged gargoyle -- 10261
//mon 10261 10 20

fire comodo -- 10283
//mon 10283 10 20

merman - 10631
//mon 10631 10 20

pasiar 11001
//mon 11001 10 20

nosiar 11011
//mon 11011 10 20

freezing walter 11074
//mon 11074 10 20

burning walter 11073
//mon 11073 10 20

electric walter 11075
//mon 11075 10 20


----------------
auch *
gavi di light id  -- 10685
//mon 10685 10 20
----------------------------

selva recruit 
-----
avalanche revenant
30461
//mon 30461 120 1

-------------------------

dr torsche/cath recruit
-

------
otite piece
class id 21170

--------------------------------------------------------
---------------------
katovic snowfield quest -
avalanche revenant
30461
//mon 19760 120 50



------
altria 
---------
rabiosa 19760
rabioso 19761
oghe 19757
ogbe 19758

viron 
-----
clock tower 
composite steel 21601 ,  cast iron 21602 


--------------------------

* add characters guide *

first

on the client side
 
what you need is
 
job, npclist, skill, stance, stancecondition
 
this is basic
 
Other items, artifacts, etc. required for the character must be additionally worked on.
 
In addition, because of the texture suitable for the character and the image of the bullet in the case of a long-distance character, xml.ipf, animation,
 
effect
 
Scripts must be written for the implementation of skills for each character.
 
Script for skill implementation
buff/attack/extraskill/coroutineskill/common_monster/common_pc/get_status_pc
 
Besides, each character is slightly different.
 
Script needs work
 
Additional client UI
Skill icon, ui internal buff tooltip, img, etc.
 
You need to work on images.


Add a dictionary accordingly

On the server side, create job, npclist, skill, stance, stancecondition + buff ies file

Script and you're done




------------------------------




      --------------
^^**^^ADVANCE QUESTS^^**^^
      --------------

** Editing Exp /drop rates etc **
Editing Exp. Rate / Drop Rate (Credit goes to marutpun2):
1. In ManagerClient_Release, ZONE@MACHINE1, choose your desired map and right click → Modify, in Param, ExpRatio xx -StanceExpRatio xx -ItemRatio xx, change xx to any number.
--------------------------------------------
How to Add Vis / Feso / Cash:
1. Play and obtain some of items and Vis first. Go to SQL, GE_DATA → Tables → dbo.ITEM, locate CLASS_ID 30000 and change the amount in COUNT. If you need Feso, change ID from 30000 to 30001 (this also applies to other items but do it at your own risk if you don't know the ID of items as it will cause you to lose the item!).
2. You can add Cash by going to RESOURCE → Tables → dbo.ACCOUNT_GOLD, fill your ID and amount of GOLD.
3. Zone between maps or go to Barrack to reflesh items and money you've changed.

--------------------------------------------------
** Finding Items Ids **
Item id is for SQL which is quite complicated.
I prefer item ClassName to use in chat which is //item ClassName qty
e.g. //item Vis 1000000000
//item CouponLv_28 1000 (Enchant Chip Master for Valeron)
//item SocketProtect 1000 (Socket Processing Tranquillizer for socketing 4 slots)
//item EXPCard_Ma_Trade 1000 (Instant lv.1 to Master)
//item EXPCard_Master_a 1000 (Exp10% for Master - this means use 100ea to reach High Master)
//item TrainingCard_G 1000 (Stance EXP)
//item TrainingCard_Ex 1000 (Expert Stance EXP)

for more items ClassName, you have to look at server folder's xml. "/rGE_server/ge/xml"
open with notepad, wordpad or your browser whichever fast enough to load the data.
these are the files that I have usually used.
- datatable_item_armor
= look for Valeron_Metal, Valeron_Leather, Valeron_Coat, Valeron_Robe
- datatable_item_earring = Valeron_Earring
- datatable_item_neck = Valeron_Neck
- datatable_item_belt = Valeron_Belt
- datatable_item_glove = Valeron_Gloves
- datatable_item_boots = Valeron_Boots
- datatable_item_artifact
= look for character name to use their unique effect i.e. search fighter for VanguardShield.
note: some new RNPCs don't have unique artifact, you can use Limit_STR or whatever instead.
- datatable_item_consume
= look for buff items ie. steroid, triumph, principal, hermes.
- datatable_item_etc
= look for some trash items that help you through quest.
- datatable_item_lumin
= I prefer absorb HP for weapon which is Lumin_Pearl4, max HP for armor which is Lumin_Bloodstone4
- datatable_item_ring
= of course,ring BUT look for Ring2 which you can enchant
e.g. Ring2_Peltast = all skill Peltast, Ring2_Peltast_Fighter = all skill Peltast and Provoke.
Sadly, some new rnpcs don't have ring2 for their character skills ,only their stances.
- datatable_item_scroll
= for stance books (Hellena's Occultism Assistance Book is bug, can't read.)
- datatable_item_weapon
= for ValeronSword, ValeronPistol etc.

Weapon, Armor, Accessory, Ring will show theirs Serial Number which is ITEM_ID in SQL and will help you to Enhance+10 and Enchant any options you want along with http://ge.sytes.net/Enchantment.php these actions can do in real time while playing.
- Enhance Weapon and Armor go to Databases > GE_DATA > Tables > dbo.ITEM_REINFORCE and edit 1 to 10.
- Enhance Accessory(Earrings, Necklace, Belt, Gloves, Boots) go to dbo.ITEM_PROPERTIES and edit Accessory Rank to 10.
- Enchant go to dbo.ITEM_PROPERTIES, this is quite boring first time but it can use copy and paste.
I recommend to enchant for real 2 times or up to have "Previous Enchant Options", it will help you later. i.e. Valeron Sword have previous like this "ATK14%, ASPD10%, CRI+2" this will show in SQL dbo.ITEM_PROPERTIIES as PrevEnchant VALUE
115001 , 14, 115002 , 10, 115003 , 2, and now the fun begins.

1. You have to know what Enchant will occur to your item. http://ge.sytes.net/Items.php
i.e. Valeron Sword options use Enchant Chip Master (ValeronMelee), click it.
You will see chance table, for EVERY VALERON MELEE WEAPONS, which has 19 ROWS.
2. You can use these rows as a reference for editing VALUE. (I think 7 options are maximum)
i.e. You want ATK50%, ASPD30%, CRI10, ATKDEMON100%, ATKUNDEAD100%, PEN5, STR5
VALUE = 115001 , 50, 115002 , 30, 115003 , 10, 115010 , 100, 115011 , 100, 115013 , 5, 115014 , 5, (notice 2 last digits sorted by rows.)
press ENTER to make sure you are done with this item.
3. Go to Barrack or change map, and back to ENCHANT MERCHANT.
Your magic will appear in Previous Enchant Options, this will require Tears of Ana (ClassName = TearsofAna)
Remember to copy VALUE for editing other melee weapons, and not every table starts with 01.
i.e.ValeronShoot starts with 20 to 39.
   
----------------------------------------------------
v28 install guide 

Pinned by Ayane ♪
Ayane ♪
1 year ago (edited)
[English]
--------------------------------------------
Installations:
1. Download all files found in https://forum.ragezone.com/f857/granado-espada-v28-00-72-a-1198186/
Or mirror link https://tinyurl.com/2vazw3bh
2. Download SQL Developer found in https://www.microsoft.com/en-us/sql-server/sql-server-downloads
3. Install SQL 2019 Developer, choose Basic Installation Type. Also install SSMS found in https://docs.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver15
3.1 Watch https://youtu.be/QsXWszvjMBM if you need help.
4. Extract rGE_server to C:\ only, be sure to add this folder an exclusion to Windows Defender and other virus protection softwares just in case.
5. Locate rGE_server\SQL and double-click 0. ODBC.
6. Run Microsoft SQL Server Management Studio 18.
7. Go to File tab (on the upper left of the screen), Open → File... to open all SQL files in their numerical ordering (1. RESOURCE,  2. RESOURCE_LOG, 3 .GE_DATA, 4. GE_LOG, 5. DATA).
8. Execute them all (or simply hit Alt +X), you can ignore the errors.
--------------------------------------------
Server Startup Procedures:
1. Locate rGE_server and run ManagerHub.bat, ManagerNode_1.bat and ManagerNode_2.bat
2. Locate rGE_server/server_release and run ManagerClient_Release.exe, ignore the warning, log in with ID foo and password bar.
3. Click + icon on the left side until you see LOCAL@MACHINE1, click at it, GLOBAL and GLOBAL WPX will show up, right-click and run them.
4. Click at ZONE@MACHINE1 and run your desired maps (you need 24GB+ of RAM in order to run all maps).
--------------------------------------------
Connecting to the Game Server with Client & Account Creation:
1. Install rGE_setup.
2. Copy all files in rGE_server/release (in C:\) to your client's release folder you just installed.
3. Go to release folder, right-click to edit serverlist.xml, correct IP Server0_IP and Server1_IP to the IP of the server (127.0.0.1).
4. Right-click rGE.exe to create a shortcut. In the shortcut's target line, add -SERVICE to the end.
5. In Microsoft SQL Server Management Studio 18, you will see GE_DATA, GE LOG, etc. in Databases.
6. Double-click RESOURCE → Tables → dbo.ACCOUNT.INFO, right-click to Edit Top 200 Rows. Create ID in MEMBER_ID and MD5 Hash of password in PASS.
For example, MD5 of 123456 is e10adc3949ba59abbe56e057f20f883e.
6.1 You can create MD5 Hash of password here, https://www.md5hashgenerator.com/
7. Go to GE_DATA → Tables → dbo.ACCOUNT_LEVEL, right-click to Edit Top 200 Rows. Fill your ID and 1 in LEVEL.
8. Go to RESOURCE → Tables → dbo.LEVEL_PERMISSION_IP, fill 127.0.0.1 in PERMISSION_IP.
9. You can log in and enjoy the game now!
--------------------------------------------
