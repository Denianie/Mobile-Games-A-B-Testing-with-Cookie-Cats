# Mobile-Games-A-B-Testing-with-Cookie-Cats 🍪🐱
Welcome to the "Mobile Games A/B Testing with Cookie Cats" project! This project dives into the analysis of an A/B test where the first gate in the popular mobile puzzle game, Cookie Cats, was moved from level 30 to level 40. We aim to assess the impact of this change on player retention.

## Problem Statement 🎮
Cookie Cats is a hugely popular mobile puzzle game developed by Tactile Entertainment. It is a classic "connect three" style puzzle game where the player must connect tiles of the same color in order to clear the board and win the level. As players progress through the game they will encounter gates that force them to wait some time before they can progress or make an in-app purchase. In this project, we will analyze the result of an A/B test where the first gate in Cookie Cats was moved from level 30 to level 40. In particular, we will analyze the impact on player retention.

## Data Dictionary 📊
Feature|Type|Description
---|---|---
**userid**|_id_|A unique number that identifies each player.
**version**|_string_|Whether the player was put in the control group (gate_30 - a gate at level 30) or the group with the moved gate (gate_40 - a gate at level 40).
**sum_gamerounds**|_integer_|The number of game rounds played by the player during the first 14 days after install.
**retention_1**|_boolean_|Did the player come back and play 1 day after installing?
**retention_7**|_boolean_|Did the player come back and play 7 days after installing?

## Results 📈
### 1-day retention

- There was a slight decrease in 1-day retention when the gate was moved from level 30 (44.8%) to level 40 (44.2%).
- Bootstrapping was used to resample and estimate the variability in retention rates. The analysis shows that the most likely retention is slightly better when the gate is at level 30.

### 7-day retention

- There was also a slight decrease in 7-day retention when the gate was moved from level 30 (19.0%) to level 40 (18.2%).
- Further bootstrapping analysis suggests a strong likelihood (100% probability) that 7-day retention is higher when the gate is at level 30.

## Conclusion and Recommendations 🛠️
- There is strong evidence that 7-day retention is higher when the first gate is at level 30 than when it is at level 40. We should not move the gate from level 30 to level 40.
- Significant proportions of players showed minimal engagement in 1-day retention (0 game rounds). Strategies such as in-app surveys could be explored to enhance player retention and engagement based on their feedback.
