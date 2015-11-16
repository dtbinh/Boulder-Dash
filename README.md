# Boulder Dash
Boulder Dash is a game created in 1984 where a character has to collect diamonds in a cave, avoiding rock falls, monsters and explosions.
When all the diamonds are collected, the player has to reach the exit.

The project is implemented using Agent Simulation techniques, especially Interactions.  
NetLogo with the IODA extension allow to implement such technologies.  
So in the game, everything is agent (player, monsters, diamonds, rocks, etc...) and every agent interact with others agents with pre-definded interactions.

# Rules
* The player (**hero**) has to collect diamonds, while moving he is digging dirt creating empty spaces. He can also push rocks. The hero is not affected by gravity.
* The **walls** are impassable obstacles. Some can be destroyed with explosions.
* The exit (**door**) looks like a unbreakable wall until all the diamonds are not collected. Then, it becomes a door and when the player go through it, he finishes the level.
* The **rocks** are stationary as long as they stay on a support, i.e. any agent (including the hero). But when there is empty under the rock it begins to fall and stop when there is something under again. If the rock falls on the hero or a monster, it produces an explosion which destroy everything (except unbreakable walls) or create new diamonds in a 3x3 square around the explosion. The rocks also roll before they fall if they are on a support but the spaces next to it and to the support are empty. Finally, a rock can be pushed by the player onto a free spot.
* The **diamonds** are collected by the player. Except that, they have the same behavior of rocks.
* The **dirt** is widely present int the environment. The player digs it as long as he progresses and can causes rocks or diamonds to fall if the dirt was a support of them.
* The **monsters** are moving with a very simple intelligence. If they touch the player, it produces an explosion (and kill the player). They are not affected by gravity and can be killed by rocks or diamonds falling.
* The explosions (**blast**) spread around them with a decreasing force. Some of them erase everything, creating empty space (all the agents are killed except unbreakable walls) whereas other create diamonds.
