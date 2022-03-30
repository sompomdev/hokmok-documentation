WAVE_REDUCE => Decrease monster wave by stage

also check [[Game Level, Wave Rule]]
also check [[Fear bunny ears]]


**Unlock and level up rule**:
- Some supporters will have this kind of skill that players can unlock at a specific level. 
- Currently the value(1 is default) of this skill is configured from SupportData.json in a property name (m_skillPercent).
- This kind of skill with supporters, can only be unlock, and cannot be upgraded. But it can be unlock again after the Evolve and its value can be increase with the evolve counter and formula that defined (SMPSupportsCharacterControl line 757)
- Supporters that have this skill to unlcok:
	- #Vorana at level 600
	- #Bottom at level 600
	- #AngkTep at level 600


**Usage**:
Its value have been keep inside global variable of BattleSystem (totalSupporterWaveReduceSkillCount). It have been used together with (totalHeroWaveReduceSkillCount) to make the (totalWaveReduceSkillCount)

=> #SMPBattleSystem (line 484)
*totalWaveReduceSkillCount = totalHeroWaveReduceSkillCount + totalSupporterWaveReduceSkillCount;*

= #SMPMonsterSystem (line 91)
*int waveRound = Mathf.FloorToInt(GetSetCurrentLv / 450) * 2;  
MaxWaveCount = SMPUserData.MAX_WAVE_DEFAULT + waveRound - battleControl.battleSystem.TotalWaveReduceSkillCount;  
if (MaxWaveCount < SMPUserData.MINIMUME_WAVE)  
{  
   MaxWaveCount = SMPUserData.MINIMUME_WAVE;  
}*
