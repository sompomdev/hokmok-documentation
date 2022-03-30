ALL_DAMAGE => Increase all damage

**Rule**:
Cumulate from all supporters  


**Usage**:
- Directly add to hero tap dmg  
	#SMPHeroLevelConfiguration (line 56)
	
- Directly add to support dps  
	#SMPSupportLevelConfiguration (line 184)
	
- Indirectly add to pet by hero tap dmg
	- Pet damage calculated by apply percentage to the tapDamage that already included ALL_DAMAGE percentage #SMPPetLevelConfiguration (line 65) #SMPInventoryPetControl (line 881)
