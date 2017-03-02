**Unreal Engine Project**  
CIS 568-002: Virtual Reality Practicum, Spring 2017  
MinJae Cho, Kunal Garg, Ray Kim, Kelly Tan, Henry Zhu

#VRy Paint
- Unreal Engine 4.14.3
- [Demo Video] (https://youtu.be/UEPmKm9dm_0)

## How to play
#### Pick a game mode in the lobby
- Shoot an arrow at a box indicating the game mode of your choice.
- You can choose between _single player_, _host game_, and _join game_.
- The box for _join game_ will only appear if the game detects a host in the local network. This box can several seconds to appear.

#### Paint the most area to win
- In order to win, you have to paint the most area in your map within the time limit.
- Destroy objects in the map to paint more area.

#### Shoot arrows
- **Vive VR** 
 - Hold both controllers up in front of you.
 - Hold down the **right trigger** and **pull back** to adjust strength.
 - Hold down the **left trigger** to toggle teleport arrow. Note that teleport is the only way to move with Vive controllers.
 - Let go of the trigger to **release** the arrow.
 - Use the **left touchpad** to look around horizontally.
- **Keyboard**
 - Press **1** to toggle normal arrow, and **2** for teleport arrow.
 - **F** to shoot, and **WASD** to move around. 

#### What arrows do
- The non-teleport arrow will paint the ground with your color.
- When an arrow hits objects in the map, like fruit stands and trees, it will destroy them.
- When an arrow hits your opponent, they will be sent back to their original spawn area.
- Teleport arrows will take you to the place where it lands.
- Teleport arrows will not teleport you if it hits objects in the environment, or the walls.

 
## Techniques used

#### Controls
- **Motion controls**
 - Motion controls provide an intuitive way to shoot arrows. As if with a real bow, the distance pulled back determines the initial speed of the arrow, and the release of the finger on the bowstring (R trigger) releases the arrow.
- **Haptic feedback**
 - The controller gently vibrates to let the player know that they’ve released an arrow.

#### Gameplay
- **Painting**
 - The ground in VRy Paint is generated using cubes. When an arrow hits the ground, we set the material of the cubes in the hit region to paint material depending on the shooter.
- **Minimap**
 - We place the minimap differently on screen and on HMD, because the 2D version obstructs the player’s view in VR, leading to discomfort. In order to reduce this discomfort, we place a minimap each in either side of the player’s peripheral vision, so that they can simply look to their side to see the minimap.
- **Teleport with fade**
 - Moving around in VR can cause motion sickness because of the inconsistency between the movement in the visual field and physical movement. Limiting movement in VR to teleport solves motion sickness.
 - Instantaneous teleport can be disorienting, and sometimes even sickening due to the sudden change. The fade protects against these unpleasant effects by making the sudden change less perceivable.
- **Game lobby**
 - Play alone, host a game, or join one in the multiplayer lobby. The game starts in the lobby, and players can choose their game mode before entering the game. Once the game is over, the player is teleported back into the lobby.


## Answers to questions
#### When in VR mode, did you feel any motion sickness? Why and why not?
- We felt motion sickness when motion tracking was not working properly. However, because we limited movement in VR to teleportation with a fade, there is little motion other than the motion that corresponds to head movement. We did not experience motion sickness under normal circumstances.

#### What was the hardest part of the assignment?
- The hardest part was getting getting multiplayer to work with our previous implementations. Because we started without any knowledge on designing a multiplayer game, fixing bugs in the game sometimes broke multiplayer functionality, and vice versa.

#### What do you wish you’d done differently?
- We wish that we focused more on simplifying our blueprints and ironing out bugs. Because we had to learn as we go, at times, we had had to resort to inelegant solutions. This led to more variables and problems down the road.

#### What do you wish we had done differently?
- It might have been useful to have had a vry simple individual “practice” Unreal assignment designed to get everyone familiar with Unreal before this assignment. Instead of learning on the go, we could have walked in with more realistic expectations and better workflow.
