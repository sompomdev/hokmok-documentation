Fear bunny ears => Decrease monster wave by stage

also check [[Game Level, Wave Rule]]
also check [[WAVE_REDUCE]]

**Unlock and level up rule**:
. SMPInventoryPassiveOverrideSkillItem (line 55)
. SMPPassiveSkillLevelConfiguration

=> Unlock at minimum stage (game level) 235
=> Can be level up in every 235 stage passed
=> And it's not base on Hero, it's not like other active skills

Ex: 
- Unlock level 1 at stage 235, then available to upgrade to level 2 at stage 470
- When switching betwen 2 heroes, nothing changed on this skill.


**Usage**:
The value of this skill is the same as its level. It have been keep inside global variable of BattleSystem (TotalHeroWaveReduceSkillCount). It have been used together with (totalSupporterWaveReduceSkillCount) to make the (totalWaveReduceSkillCount)

=>SMPBattleSystem (line 484)
*totalWaveReduceSkillCount = totalHeroWaveReduceSkillCount + totalSupporterWaveReduceSkillCount;*

=>SMPMonsterSystem (line 91)
*int waveRound = Mathf.FloorToInt(GetSetCurrentLv / 450) * 2;  
MaxWaveCount = SMPUserData.MAX_WAVE_DEFAULT + waveRound - battleControl.battleSystem.TotalWaveReduceSkillCount;  
if (MaxWaveCount < SMPUserData.MINIMUME_WAVE)  
{  
   MaxWaveCount = SMPUserData.MINIMUME_WAVE;  
}*


