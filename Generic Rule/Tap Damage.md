Player tap damage on the Enemy

TapDamage depending on Hero level

Tap Damage can get bonus from:

- from fairy or lucky bird #luckyBirdBonus
- anger of god skill #heroSkillBonus
- tap period combo #tapComboBonus
- item equipment #itemEquipBonus
- support skill #supportSkillBonus
- pet skill #petSkillBonus

**Existing implemenation**
For bonus from 
	- item 
	- support 
	- and pet
direclty modify the original **tapDamage**, other bonus are added when using only. That mean all the display for tapDamage will include the bonus from those 3 already.

So other bonus that add after will also take into account those 3 in the mutiplication

**First**
#SMPHeroLevelConfiguration (line 33)
#tapDamage = #tapDamage x (1 + #itemEquipBonus + #supportSkillBonus + #petSkillBonus )

**Second**
#SMPBattleSystem (line 747)
#tapDamage = #tapDamage x (1 + #luckyBirdBonus + #heroSkillBonus + #tapComboBonus )