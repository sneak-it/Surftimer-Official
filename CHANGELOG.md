# Changelog

[2021-08-05 - Version 3.2.0]
---
- New database layout for checkpoints (max 128) and storing prespeed for players
- MaxSpeedZone now limits speed acording to it's prespeed setting, it also works in XYZ
- Added optimization sql file to reduce database size
- When completing map or bonus in Practice mode will now compare time to SR and PB
- Fixed stage command
- Added chat options menu in options menu (confusing?)
- Added small hud option (might be broken sometimes, i think) in !options -> HUD Options -> Small HUD

[2021-07-17 - Version 3.1.9]
---
- Added new radio command to block list
- Removed discord webhooks for bugs, call admin, server map record, server bonus record.
Please use [Sarrus1's plugin](https://github.com/Sarrus1/SurfTimer-discord)

[2021-05-30 - Version 3.1.8]
---
- Fixed bug when teleporting to stages

[2021-05-27 - Version 3.1.7]
---
- Fixed Player profile map completions
- Fixed `ck_allow_checkpoint_recreation` not applying correctly

[2021-05-26 - Version 3.1.6]
---
- Changed the way savelocs are saved, from a server based system to a player based system
- Added time comparisions when in practice mode
- Added the ability to recreate other players savelocs by using `sm_addsaveloc` / `sm_addloc` followed by the various inputs required to recreate the saveloc
- Added the ability to clear savelocs by using `sm_clearsavelocs` / `sm_clearlocs`
- Added `ck_allow_checkpoint_recreation` to enable server owners control over allowing checkpoint recreation and how they want it to be impelemented
- Changed the way savelocs are created when spectating a player/bot. You will now create the saveloc with the time that the player/bot had at that point. This will allow you to teleport to the saveloc and receive the time the player/bot had instead of the timer just starting at 0
- Changed how practice mode works when leaving start zone. Before it would allow you to start a run in practice mode but now it will kick you out of practice mode and start the run normally
- Changed a few of the HUD colours
- Fixed CSD again

[2021-04-13 - Version 3.0.5]
---
- Added `ck_sound_record_type` to enable controll over record sounds by @Kyli3Boi
- Fixed Center Speed Display by @Kyli3Boi
- Changed permissions for `sm_fixbot` by @Kyli3Boi
- Fixed bug where you couldn't spectate highest rank player by @Kyli3Boi and @qawery-just-sad
- Fixed missed PB message for styles by @qawery-just-sad
- Fixed creating database by @qawery-just-sad

[2021-03-01 - Version 3.0.2]
---
- New Discord announcemnets with embeds Thanks to @Sarrus1, improved with style by @Kyli3Boi, added steam profiles by @qawery-just-sad
- Added style shortcut commands
- Fixed missing speed after completing a stage by making HUD bigger
- When checking profiles rank is displayed correctly
- Fixed all stages displaying double the amount Thanks to @KristianP26 for noticing this
- Removed Vote Extend
- Fix for styles being set back to default movement Thanks to @LubricantJam
- Fixed db mapcycle Thanks to @fluffyst
- Fixed sspec Thanks to @LubricantJam
- Changed noclipspeed to be per player Thanks to @qawery-just-sad
- Added delete records by STEAMID Thanks to @Bara, @dPexxIAM
- Added Telefinder by marcowmadeira
- Fix for Knife spam Thanks to @Kyli3Boi
- Added AutoExecConfig Thanks to @Kyli3Boi, @Bara
- And many more bug fixes, optimalisations Thanks to @Bara, @LubricantJam, @PwnK, @sneak-it, @dPexxIAM, @qawery-just-sad

[2020-04-24 - Version 285]
---
- Created and updated the changelog to version 285. @olokos
- Updated readme
- Use short coded colors for center hud
- **Replace old enum arrays with enum structs - Huge thanks to @Bara**
- Quake sounds fix Thanks to @samatazz Stops ALL sounds being played if the user has it turned off in their configs
- Removed trails chroma from surftimer's code. You now have to install trails chroma separately. Thanks to @13ace37 and @Bara
- Updated colorvariables.inc in release binary and Readme.md with a fork by @olokos which merges all pull requests on the original repository and adds cksurf colors to it.
- Fixed speed disappearing between stages and on startzone, by removing blank font class from the center hud code.
- Compiled with latest PTaH and DHooks includes, if such are used by the code.

[2020-04-22 - Version 284]
---
- Actions: Actually download includes for building with GitHub actions
- Actions: Thanks to @Bara actions will now download the entire repo containing the includes, instead of just some of them
- Updated plugin URL to the current repository
- Removed z4lab tags from SurfTimer.sp, since it now is a community-oriented project
- Add new radio commands to block list @sneak-it
- Fixed prespeed exploit Thanks to @sneak-it
- Removed hardcoded entity kill list, we suggest using stripper instead
- Actually started making use of GitHub releases page :smile:

[2020-04-18 - Version 283]
---
- Fix !starpos command braking staged maps Thanks to @ashakiri-dev
- Massive optimizations to queries, which helps with DB performance a lot! Thanks to @ashakiri-dev #6de0d5b

[2020-04-17 - Version 282]
---
- Fixed trails-colors.cfg error message
- Added variable replay bot delay (ck_replay_bot_delay to set delay with which bots will join the sever)
- Updated bug report template
- Remove duplicated query
- Added style Freestyle
- Implemented tier 7 & 8 system
- Fixed casing for !help command
- Updated readme
- Added Orchid color declaration (Is it really 0x1A though?)
- Possibly fixed HSW
- Workaround for invalid data pack type ( http://github.com/z4lab/z4lab-surftimer/issues/98 )
- Remove unndeded space that caused an error
- Corrected some typos
- Added github actions to repository, big thanks @Bara
- Remove sourcemod includes from the repository
- Update gitignore
- Replaced deprecated functions
- Fix base64.inc compile issue with SM1.11
- Added onejumplimit remover to mapsettings
- Fixed the speed of prespeed displaying multiple times
- Fixed a memory leak thanks to @covertxd
- Fix sql errors when server name has symbols @sneak-it
- Repository cleanup - removed external dependencies and includes
- Remove unnecesary locking of queries in favor of SQL_SetCharset 
- Dont lose last seen data when migrating to the new SQL structure using upgrade.sql
- Fix delimitations in upgrade script
- Fix upgrade script for CentOS
- Updated upgrade script to point to this repo.
- Fix SQL Hostname Error Thanks to @sneak-it
- Removed sourcecomms includes
- Removed TF2 and Base64 includes
- _FIX BIG MEMORY LEAK s/o GAMMACASE, KiD-Fearless_ THANKS TO @sneak-it #996ef60
- Remove broken SQL query set name
- We dont support SM1.11 really, make it obvious in Readme aswell.

[2020-04-05 - Version 281]
---
- Fixed sourcemod compiler warnings
- Change the repo to z4lab
- Added missing texture files
- Fixed typo in queries.sp
- Updated gitignore
- Updated cleaner.cfg
- Now SurfTimer supports MySQL8+ - ranks and groups were used in queries, but are reserved MySQL keywords. Bacticks had to be used.
- Updated Readme

[2019-11-20 - Version 280pre]
---
* **[UTIL]** Updated GeoIP.dat
* **[UTIL]** More code cleanup (WIP)
* **[FIX]** Useless error log spam (cleaner.cfg)
* **[FIX]** Fixed `maxvel` bug
* **[FIX]** VIP chat spam bug
* **[FIX]** "fixed" colors in the center panel
* **[NEW]** added/fixed "one jump limit" for new speed style
* **[REQUEST/NEW]** added `sm_newmaps` and `sm_addnewmap` command
* **[FIX]** disabled auto-reset while surfing in style
* **[UTIL]** removed some typos

[2019-08-18 - Version 274]
---
* **[NEW]** added `sm_autoreset` command

[2019-08-16 - Version 273]
---
* **[REQUEST/FIX]** Finally fixed maxvelocity bug ._.

[2019-08-14 - Version 272]
---
* **[REQUEST/FIX]** Fixed VIP chat spam bug
* **[UTIL]** Changed VIP system

[2019-08-13 - Version 271]
---
* **[REQUEST/FIX]** Fixed `sv_maxvelocity` bug
* **[REQUEST/FIX]** Fixed prestige avoid for vips

[2019-08-12 - Version 270]
---
* **[UTIL]** Combined config files and removed old settings like bhop and such
* **[UTIL]** Added external dependencies for compiling (dhooks, steamworks, discord_api, cleaner)
* **[NEW]** Added "Silence Spec" usable with `sm_silentspec` and `sm_sspec`
* **[NEW]** Added [Trails Chroma](https://github.com/Nickelony/Trails-Chroma) into the SurfTimer for VIP's and Admins
* **[NEW]** Added trails for replay bots
* **[REQUEST/NEW]** Added ConVars for both discord records announcement webhooks
* **[REQUEST/FIX]** Fixed admin tags without country tags
* **[REQUEST/NEW]** Added command to toggle triggers while noclipping
* **[FIX]** Maybe mapchange fix

[2019-08-02]
---
* **[RELEASE/NEW]** added chat command for each option in miscellaneous options [#1](https://github.com/z4lab/z4lab-surftimer/commit/075694a9af16bc8772992dcc3c6fe833192806e6) - [Todo](https://github.com/z4lab/z4lab-surftimer/issues/38)
* **[RELEASE/FIX]** fixed and made cp/wrcp messages toggleable  [#1](https://github.com/z4lab/z4lab-surftimer/commit/1cdb099c87b24bf201add111f2cb8123b45555d6) - [#2](https://github.com/z4lab/z4lab-surftimer/commit/808871c5617449de86c074737a193e2ea2610c33) - [Todo](https://github.com/z4lab/z4lab-surftimer/issues/39)

[2019-07-31 - 2019-08-01]
---
* **[RELEASE]** Release [261](https://github.com/z4lab/z4lab-surftimer/tree/261)
* **[RELEASE]** Release [260](https://github.com/z4lab/z4lab-surftimer/tree/2.6)

[2019-07-30]
---
* **[REQUEST/FIX]** fixed default_title name color [#1](https://github.com/z4lab/z4lab-surftimer/commit/4381c12b61fba33ed678f61f648d5f870c1e79b3) - [Request](https://github.com/z4lab/z4lab-surftimer/issues/24)
* **[REQUEST/NEW]** return to dr menu after delete [#1](https://github.com/z4lab/z4lab-surftimer/commit/ae632a2c43d8ee9fbb9f81590cca44bc15c409d0) - [Request](https://github.com/z4lab/z4lab-surftimer/issues/27)
* **[REQUEST/NEW]** made it possible to remove remove protection at sm_dr [#1](https://github.com/z4lab/z4lab-surftimer/commit/83c01b34f124a4199fae3e730476374a94d14943) - [Request](https://github.com/z4lab/z4lab-surftimer/issues/27)

[2019-07-20]
---
* **[BUG]** fixed @ in chat [#1](https://github.com/z4lab/z4lab-surftimer/commit/fed31a8b9c06d94fad5414c591a748ccb142c463)
* **[REQUEST/DC]** made calladmin/bug webhooknames changable [#1](https://github.com/z4lab/z4lab-surftimer/commit/ece5ffcb5d64b17c86ff1f196fcf6e592369c907) - [Request](https://github.com/z4lab/z4lab-surftimer/issues/23)

[2019-05-22]
---
* **[NEW]** disabled triggers while noclipping [#1](https://github.com/z4lab/z4lab-surftimer/commit/a4065177b8c2453e4fe6249a514dba1f79bf55a2)
* **[BUG/UTIL]** a few fixes [#1](https://github.com/z4lab/z4lab-surftimer/commit/43d7dbe58bb485f8bf7856d05ddd46c178618319)

[2019-05-06]
---
* **[UTIL]** repo housekeeping [#1](https://github.com/z4lab/z4lab-surftimer/commit/dc7a0a9fe631e20c81c18182c720392b50236804)
* **[PRE]** sourcemod 1.10 fixes [#1](https://github.com/z4lab/z4lab-surftimer/commit/b31ff454b9182d2e4b3b96fb555f309732945fd7)

[2019-04-25]
---
* **[UTIL]** forced clantags to normal style [#1](https://github.com/z4lab/z4lab-surftimer/commit/d030af6ba92a89a6f55448346accf52fb5118db2)
* **[BUG]** fixed admin clantags [#1](https://github.com/z4lab/z4lab-surftimer/commit/4848dff2e0b95884da580286bacb4822069eb8e5)

[2019-04-23]
---
* **[BUG]** fixed enforced clantags @ tablist [#1](https://github.com/z4lab/z4lab-surftimer/commit/e0012df4f25916bc6502d55806e9124f6c35e521)
* **[BUG]** fixed s1 to s2 bug [#1](https://github.com/z4lab/z4lab-surftimer/commit/d7892b7aadbbde5a4d8f6802471f7be5791c12a7)

[2019-03-22]
---
* **[NEW]** added prestrafe message to db [#1](https://github.com/z4lab/z4lab-surftimer/commit/992abc555895ea835070e47ced69efd8508c0ec6)

[2019-03-21]
---
* **[NEW]** added prestrafe message [#1](https://github.com/z4lab/z4lab-surftimer/commit/385ccbe8d187e3ac0904eb7776df76a726118983)

[2019-03-19]
---
* **[DC]** changed webhook cvar [#1](https://github.com/z4lab/z4lab-surftimer/commit/7f5ca1dd1f170aa50359edd340ca98e25029d8a6)
* **[DC]** added bonus announcement [#1](https://github.com/z4lab/z4lab-surftimer/commit/a30fb691121ace576134c27e26fd5ddb70171f60)

[2019-02-18]
---
* **[STYLE]** clean up [#1](https://github.com/z4lab/z4lab-surftimer/commit/bb78a4478337a504d5521b8ecec58c0623877751)
* **[STYLE]** changed spec keys [#1](https://github.com/z4lab/z4lab-surftimer/commit/f88a0a77ab972b9c25fec1c39ceeb95c655c8c4d)

[2019-02-17]
---
* **[UTIL]** removed last timeleft seconds [#1](https://github.com/z4lab/z4lab-surftimer/commit/6f73aca9b84105f0f883c1e257859af54510cc80)

[2019-02-16]
---
* **[DC]** fixed calladmin messages [#1](https://github.com/z4lab/z4lab-surftimer/commit/ede06c446bdac87b3c826691a5cb0f8124bdf7b7)
* **[STYLE]** wr => sr [#1](https://github.com/z4lab/z4lab-surftimer/commit/621b8003fb5a3c8356271205492f274499b0f2a3)
* **[STYLE]** nord colors [#1](https://github.com/z4lab/z4lab-surftimer/commit/195e4cdd88d7b940a8c345497a438814189b7c62)
* **[STYLE]** wr => sr [#1](https://github.com/z4lab/z4lab-surftimer/commit/4b4d2fdcf9cf6d84503a695a18f30a6037e9e33d)

[2019-02-14]
---
* **[STYLE]** wr => sr [#1](https://github.com/z4lab/z4lab-surftimer/commit/ec0abddcf0508a86305fa618bd0f099c7a60fec5) - [#2](https://github.com/z4lab/z4lab-surftimer/commit/ff816ab14928f390f361d7cffd0b8e4a9901944c)
* **[STYLE]** nord colors [#1](https://github.com/z4lab/z4lab-surftimer/commit/bb5ec236f807ddfdf87adf4f19d00d0a187007ab)

[2019-02-13]
---
* **[STYLE]** nord colors [#1](https://github.com/z4lab/z4lab-surftimer/commit/a08650ff6f091df69d88afb6040af0858d2f63ab)

[2019-02-12]
---
* **[STYLE]** nord colors [#1](https://github.com/z4lab/z4lab-surftimer/commit/d5aad915d5a799cd0ca7418ec5c4eae2d311f707)
* **[UTIL]** code cleanup [#1](https://github.com/z4lab/z4lab-surftimer/commit/7342d245c6d5ba48fcc10da77ef59b151117e254)

[2019-02-11]
---
* **[DC]** changed layout of discord bug/calladmin messages [#1](https://github.com/z4lab/z4lab-surftimer/commit/16430e1be29e4497295d3b99a256baa98f2da6d4)

[2019-02-10]
---
* **[DC]** changed layout of discord record announcements [#1](https://github.com/z4lab/z4lab-surftimer/commit/a601fbe1208795a294075929b3a5d43e3ff23155) - [#2](https://github.com/z4lab/z4lab-surftimer/commit/e40050f25cf6eeb3c12df51a04b9c48c575e91c1) - [#3](https://github.com/z4lab/z4lab-surftimer/commit/6d61bdc6e926c94b863550300b021e672844a4c6)
