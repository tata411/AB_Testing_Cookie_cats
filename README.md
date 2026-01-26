# Cookie Cats A/B Testing Project
Cookie Cats is a hugely popular mobile puzzle game developed by Tactile Entertainment. It's a classic "connect three"-style puzzle game where the player must connect tiles of the same color to clear the board and win the level. It also features singing cats. As players progress through the levels of the game, they will occasionally encounter gates that force them to wait a non-trivial amount of time or make an in-app purchase to progress. In addition to driving in-app purchases, these gates serve the important purpose of giving players an enforced break from playing the game, hopefully resulting in that the player's enjoyment of the game being increased and prolonged.
But where should the gates be placed? Initially the first gate was placed at level 30. In this project, we're going to analyze an AB-test where we moved the first gate in Cookie Cats from level 30 to level 40. In particular, we will look at the impact on player retention.

## Project Overview

The purpose of this project is to conduct an A/B test comparing two different versions of a game level. The test seeks to answer the following question:
- **Does the placement of the gate (level block) in the game impact player engagement, as measured by the number of rounds played (`sum_gamerounds`)?**

The results will help determine if there is a statistically significant difference between the two versions and guide the company on which version to continue using.

## Dataset

The dataset `cookie_cats.csv` contains the following columns:

- `userid`: Unique identifier for each player
- `version`: The game version the player interacted with (either `gate_30` or `gate_40`)
- `sum_gamerounds`: Number of game rounds played by the player
- `retention_1`: Whether the player returned the day after installing the game
- `retention_7`: Whether the player returned seven days after installing the game
