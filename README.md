**Unreal Engine Project**  
CIS 568-002: Virtual Reality Practicum, Spring 2017  
MinJae Cho, Kunal Garg, Ray Kim, Kelly Tan, Henry Zhu

#VRy Paint
- **Unreal Engine 4.14.3**

##February 9, 2017: Work Plan
####Think through all the technical requirements of the aforementioned steps for this project. Write down and elaborate on what tasks will take what amount of (estimated) time. Be thorough here so we can give you good feedback.
- Task and Time Estimate
 - The alpha mechanic demo is only a week away, so the arrow shooting mechanism is the first thing we should focus on.
 - How do we collaborate? Is using branches and pull requests hard? Can any of you teach me (is using dropbox bad)
 - We need to come up with a way to avoid working on the same blueprints at the same time. Splitting up the work into chunks is important. We’ll just combine the work for the shooting into many chunks and merge frequently for the first part cause the deadline is next week. Example (getting the arrow part to work) - a person works on animation of the bow based on how far the bow is pulled back, another works on how far the arrow travels based on power, another person (if possible 2) work out how movement should be done.
- Multiplayer and gameplay mechanics (respawn…) What type of game is this? FPS arena game like Quake? Or a game like Overwatch (team based) (multiplayer ~ a week? - gameplay ~ decide over time?)
 - We need to make a character so that the players can see each other. Can we just have floating things instead?


####Divide up the work between your team members according to the technical requirements mentioned above.
- Actual splitting will take place after we have a better idea of what we need to do for the project.
- Individual preference:
 - Henry: I have some experience with networking and multiplayer from using the Unity game engine (a few years ago...) and could implement some gameplay mechanics
 - Minjae: I can make the video, and would like to work on visual style, UX and shooting mechanism. - Kelly: I can try to work on the haptic/visual feedback.  Can also help with the arrow shooting/switching mechanisms.
 - Kelly: I can try to work on the haptic/visual feedback.  Can also help with the arrow shooting/switching mechanisms.
 - Kunal: I would like to work on the shooting mechanism or scene design


####Invent your own mechanics and visual style - what will the win and loss conditions be? Do you have a preferred appearance for the world and for the player?
- Invent your own mechanics and visual style - what will the win and loss conditions be? Do you have a preferred appearance for the world and for the player? 
- Mechanics - The user has to press a button on one of the controllers to start pulling the bow string. Once pulled back, the user can release that button to let go of the bow string, which releases the arrow. Additional button held down could be used to toggle between the types of arrows. 
 - Idea: the bow could appear when the button is pressed. Could use either hand. 
 - Initial velocity of arrow based on how far the user pulls back. 
 - Should we be changing direction based not on the raycast but on where the other controller is?  
  - Yeah we could calculate the angle between the controllers or something to control the angle 
  - Crosshair preview of where arrow will land/trajectory drawn. 
 - Question: for arrow shooting, can we make them infinite? Or do you want us to implement a recharge mechanism? - Recharge mechanic could be better, pick up the arrows that randomly spawn on the ground 
  - If picking up from ground, we need to create a mechanism for picking things up… just walking over or some kind of interaction?  Maybe if it’s within a certain radius you can look at it and press a button. 
- Visual style - Work with starter content as much as possible, and go for simpler geometries. Make style decisions later on. 
- Win/loss - For the prototype stage we should just brainstorm and try to decide on an idea.  
 - Cliche one is to just have health point, and after limited time / arrows compare the remaining health point. 
  - Shooting at each other may be difficult. 
 - Like those typical tutorial for Call of Duty or Overwatch. Dummy dolls can pop up and gain points by destroying those  dummies. And dummies in harder place to reach have higher points <= these ones require teleport to get closer for example/ 
 - Another idea is if you’ve ever seen the game splatoon like trying to “paint” as much of the world as you can.  That way it’s more like a world exploring thing but also with an objective.  Hitting the other player with paint stuns them for a little. 
  - Could make terrain different every level.  Also doesn’t necessarily need levels. 
  - What should be the single player objective be? 
   - Boring option is like a time trial or something.  See how much you can cover in a certain amount of time. 
- Could we put a unique twist on this that is only possible in VR. 
 - Maybe we could have like occasional floating paint balloons that if they shoot them it like explodes paint. 
- World - we need a decently sized map with varied height, so that the user can shoot at various angles. There should also be obstacles to hide behind.


####How will you meet the timeline described below?
- Get the arrow/shooting mechanic done by weekend (preferably saturday) Split the arrow arc/distance/stuff implemented by one part of the team (2?) and the bow animation and xbox360/VR done by another part of the team (3?). Then merge the result and test on sunday?
 - I think we can use the gun in the starter content… the bullet travels like a ball… I think we can just use that and make it look like an arrow
- Tasks Listed in order: 
 - Creating the shooting mechanism
 - Add mechanic for recharging arrows, smooth out controls for arrow/bow interaction.
 - Add teleportation (bow) (Most important). 
 - Begin level design. 
 - Basic multiplayer interaction for at least 2 players. 
- Basic gameplay should work at this point. Flesh out gameplay and see what cool stuff could be added to the game. Level design should be almost done. Add more visual effects. Multiplayer has to work well (barely any lag (rubberbanding) and responsive)

