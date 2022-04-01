- Player farm gold by tapping to kill monsters
- Gold drop after the monster is dead

Gold or coin drop formula #SMPEnemyLevelConfiguration (line 134)

Amount of gold to drop can be increase with bonus
- From equipment item #itemEquipBonus 
- From support skill #supportSkillBonus 
- From pet skill #petSkillBonus 
- In term of chest gold #chestGoldBonus

**Existing implementation**
- Type monster
	#totalCoin = #originalFormula

	Monster die
	#coinToDrop = #totalCoin  x (1 + #itemEquipBonus + #supportSkillBonus + #petSkillBonus )
	
- Type Golden chest (rabbit)
	#totalCoin = #originalFormula + #chestGoldBonus 
	
	Each attack
	#coinDropEachTap = value x (1 + #itemEquipBonus + #supportSkillBonus + #petSkillBonus )
	
	#coinRemaining = #totalCoin - #coinDropEachTap 

	Golden chest die
	#coinToDrop = #coinRemaining x (1 + #itemEquipBonus + #supportSkillBonus + #petSkillBonus )