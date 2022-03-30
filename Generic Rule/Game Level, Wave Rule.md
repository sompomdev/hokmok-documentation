**Game Wave Rule**
MAX_WAVE_DEFAULT = 10
MINIMUME_WAVE = 6

- 1 game level has 10 waves to pass
- Number of waves will be increased +2 in every 450 levels passed #SMPMonsterSystem (line 91)
- Number of waves can be reduced with hero passive skill [[Fear bunny ears]] and Supporter skill [[WAVE_REDUCE]]




**Number of waves will be increased +2 in every 450 levels passed**

MAX_WAVE_DEFAULT = 10
MINIMUME_WAVE = 6

int waveToAdd = (currentLv / 450) * 2

int totalWaveReduce = fromSupportSkil + fromHeroSkill

int totalWave = MAX_WAVE_DEFAULT + waveToAdd - totalWaveReduce

if (totalWave <MINIMUME_WAVE) totalWave = MINIMUME_WAVE