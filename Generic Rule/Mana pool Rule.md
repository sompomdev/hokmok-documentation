- Mana pool is disabled at the beginning of the game
- Mana pool will be activated when player unlock skill that provide mana cap
- Active skill of hero will consume mana to activate its power
- Mana pool is empty for fresh activated, then it start filling by mana rate (per minute) little by little until ful (max cap depending on the unlock active skill of hero [[Main Hero Skills]])

- Mana pool can refil from:
	These items will go togther increase fill rate per minute
	- Default 3 rate per minute
	- Support skill ([[MANA_BONUS]]), with 1 refil rate
	- Number of monster have been killed per minute (>= 12 => give 1 rate)
	- Mana rate can also get from Equipment item that player can purchase
	
	
	There is a perk that can help to refil mange completely [[Mana Portion]]
	
	#SMPManaLevelConfiguration (line 38)