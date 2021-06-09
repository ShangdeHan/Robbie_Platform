# Game Basic Information #

## Summary ##

This game is called “Robbie Swifthand and the Orb of Mysteries”, and there’s already a finished version on steam. Basically, this is an adventure game based on multiple levels. On the way to pass the level, the players have to think the way they want to go, and there might be tricky ones! After knowing the correct way, the player also needs to try their best to get rid of various kinds of obstacles, such as swing axes and spikes. I think this game is very challenging although the mechanics are not complicated, and I believe this is the most attractive part of the game: “Easy but difficult”. After clearing all the levels, the plays will get a sense of achievement, and that is our goal of designing. For what we need to do, is designing absolutely new levels, and totally self-designed maps. Moreover, we added some new features in this game. For example, we make the player invincible when he’s hanging on the wall, and give more possibilities for the player to reach the goal. What’s more, we added more kinds of obstacles than were in the original game, and I think that will make the game more challenging. I wish every player can try hard and enjoy the game!


## Gameplay Explanation ##

**In this section, explain how the game should be played. Treat this as a manual within a game. It is encouraged to explain the button mappings and the most optimal gameplay strategy.**


**If you did work that should be factored in to your grade that does not fit easily into the proscribed roles, add it here! Please include links to resources and descriptions of game-related material that does not fit into roles here.**

Play Method:
Method 1: Go to Executable Game file and download RobbieGame.zip file to play directly.
Method 2: Download all GitHub file and open it from Unity.

Game play:
"A" or "←": Move left.
"D" or "→": Move right.
"Space": Jump.
"Ctrl": Crouch.
"Space" after "Ctrl": Jump higher.
"Ctrl": if you are hanging on the wall, press "Ctrl" to drop down.

Props:
Orb: Door only opens after getting enough orbs.
Skills:
Keep press button "Ctrl" and move right or left a little then jump will jump higher.
Easter Egg:
You will get a easter egg after completing all three levels.

Tips:
Based on our design, you only can change music volume at the begining of the game.
Estimated game time

Level 1: About 5 mins

Level 2: About 8 mins

Level 3: About 12 mins

The core gameplay system is to explore adventure. By controlling the thief, the player will explore and take an adventure of the temple and each different level. When the player is playing our game, he / she can walk, collect items which are the shiny coins, and avoid obstacles. And the time recorder on the top right would record your time for each level so you can challenge yourself every time. And the coin collector recorder would record how many coins you have collected in each level. Overall, this game will challenge the player’s skill to stay alive and complete the mission.
Here is the diagram to show the core gameplay system of our game. In this diagram, we can see that the player will start from the beginning place and it needs to collect the coins / avoid the obstacles and find a way out in each level. If you die, then you will restart at the beginning place. If not, you will enter into the next level. After you have found all the ways out, the game will pop out the reminder showing that you have finished all missions and you have got out the temple successfully. It’s basically like a loop. If you die then loop over again and again until you have met all the requirements to get out or you will be stuck in this dark temple forever.

In this game, the main part is the tilemap and the script parts. Since it is a 2D exploring/adventuring game, it is really important to design both interesting and exciting game maps for the players to dive into. Beyond the first 2 levels which were reimplementing the existing levels, we created level three which is way harder and more interesting than the previous two levels. Although level 3 might seem a little bit too hard for those who are new to the game, we hope the game is not an easy one and people can gain more interest as they restart the game again and again. 
When the player is gathering the coin, the audio manager and other managers will make the sound to acknowledge the player (and also touch other things or die) and keep the record of how many coins did the player get and how much time did the player used to complete each level. 
We wish our game can provide players with an exciting adventure by adding all the UI, Input, Art, Music, etc altogether. 
Hope you guys like our idea and enjoy the game!


# Main Roles #

Your goal is to relate the work of your role and sub-role in terms of the content of the course. Please look at the role sections below for specific instructions for each role.

Below is a template for you to highlight items of your work. These provide the evidence needed for your work to be evaluated. Try to have at least 4 such descriptions. They will be assessed on the quality of the underlying system and how they are linked to course content. 

*Short Description* - Long description of your work item that includes how it is relevant to topics discussed in class. [link to evidence in your repository](https://github.com/dr-jam/ECS189L/edit/project-description/ProjectDocumentTemplate.md)

Here is an example:  
*Procedural Terrain* - The background of the game consists of procedurally-generated terrain that is produced with Perlin noise. This terrain can be modified by the game at run-time via a call to its script methods. The intent is to allow the player to modify the terrain. This system is based on the component design pattern and the procedural content generation portions of the course. [The PCG terrain generation script](https://github.com/dr-jam/CameraControlExercise/blob/513b927e87fc686fe627bf7d4ff6ff841cf34e9f/Obscura/Assets/Scripts/TerrainGenerator.cs#L6).

You should replay any **bold text** with your relevant information. Liberally use the template when necessary and appropriate.

## User Interface (Name: Shangde Han)
I implemented many different functions and UI designs. For the orbs icon, there is a function to count the total orbs [UpdateOrbUI](https://github.com/ShangdeHan/ECS189_FinalProject/blob/main/RobbiePlatform/Assets/Scripts/UIManager.cs#L22)

Music volume slider: I designed a slider to let player control the music volume from low to high. 

There is a "Pause" button on the top of the screen. Player can click that button or "ESC" on keyboard to open or close the Pause Menu. In the menu, there is a music volume slider that player can control to adjust the music from low to high. In addition, there are some tips, such as move, jump, crouch to help player know how to play this game. What's more, there is a "Resume" button can let player continue to play game. And also there is a "Quit" button to let player quit the game if the player play in the game. 



## Movement/Physics (Chongwen Wang)

In our game, the basics of movements we have are ```go left/right```, ```jump```, and ```crouch```. And some special movement such as ```crouch jump``` (jump higher) and ```catch the edge of the floor```. All these movements were implemented in [PlayerMovement.cs](https://github.com/ShangdeHan/ECS189_FinalProject/blob/0c1dc38227404291f04ace6146d4f7b8cbb8a671/RobbiePlatform/Assets/Scripts/PlayerMovement.cs). 


This movement script does not use any standard physics model and physics system. For what I did, I just implemented all basic movements that make the game playable. Then I implemented some advanced movements to make the game process more flexible. First, the super jump will be applied when the player clicks the jump button when holding the crouch. To implement this skill, I [added force]( https://github.com/ShangdeHan/ECS189_FinalProject/blob/0c1dc38227404291f04ace6146d4f7b8cbb8a671/RobbiePlatform/Assets/Scripts/PlayerMovement.cs#L177) to the character to let him jump higher than usual. Second, floor catching, the player can catch the floor, this is a skill to help the player enter the higher floor.  furthermore, I also implement a function call [physicsCheck](https://github.com/ShangdeHan/ECS189_FinalProject/blob/0c1dc38227404291f04ace6146d4f7b8cbb8a671/RobbiePlatform/Assets/Scripts/PlayerMovement.cs#L82) that used ray to check each side of the character. The ray helps me to figure out which side of the player is touching the wall or floor. All movement will display differently when there is a touching.


To have the best performance, player’s movement will display differently according to the situation. Some physics elements will change to make these movements look more similar to real-world movements, such as velocity. When the character is crouching, the speed of walking will [decrease]( https://github.com/ShangdeHan/ECS189_FinalProject/blob/0c1dc38227404291f04ace6146d4f7b8cbb8a671/RobbiePlatform/Assets/Scripts/PlayerMovement.cs#L122). 


## Animation and Visuals

**List your assets including their sources and licenses.**

**Describe how your work intersects with game feel, graphic design, and world-building. Include your visual style guide if one exists.**

## Input
Just like most of the games, A means moving left, D means moving right, Space means a single jump, Cril means crounch, Crtl plus Space means double jump, and also
if you are hanging on the wall then just press Crtl to drop off the wall.

## Game Logic (Shijiao Song)
Design the levels and obstacles of the game including the size and style of maps, the ways to win the game. Also, control the difficulties between levels, and make players feel good while playing.

Many of the game data comes from the Assets store of Steam, and some of them are designed by me.

# Sub-Roles

## Audio

**List your assets including their sources and licenses.**

**Describe the implementation of your audio system.**

**Document the sound style.** 

## Gameplay Testing (Shijiao Song)

After a few tests by myself, and some tests done by my friends and TA, I found some problems and we fixed it.

1. We fix the volume bar so that it can correctly change the volume of the game.
2. We give specific game play instruction in the pause menu.
3. We fixed a minor bug that may cause player stuck in the wall.
4. We also add the total numbers of levels description in the pause menu.
5. We enable player to call the Pause menu when press "Esc", and resume the game with "Esc".
6. We changed the success picture so that it will be more coherence with the overall theme.
7. We reconsidered camera type, and resized it to make the goals and obstacles clear.

Moreover, we changed some obstacles to make the game difficulty more suitable for players.

## Narrative Design (Chongwen Wang)

For the narrative design, I design a background story that help our team design the gameplay logic, game levels, and make player have a better game experience. By knowing the background, player can figure out their final mission of the game.  

The background story is: Robbie left his home since childhood. In order to survive, he needs to find food by stealing. After years of experience, Robbie has super athletic ability and a smart brain and became a well-known local robber. One day, someone found Robbie and wanted to hire him to steal gems in an underground warehouse of a rich man. After the mission is completed, Robbie can get a lot of money and no longer worry about survival. Robbie does not want to give up this chance, so his adventure begins…

The narrative present in game levels. In each level, people need to collect gems/coins in order to go to the next level. The reason why Robbie is taking these gems is that these gems will bring him a better life. And the map of each level was designed based on the underground warehouse.  

Also, the narrative present in game movement, such as some special skills Robbie has. Super jump (crouch- jump) reflects the reason why Robbie becomes a well-known local robber. 

## Press Kit and Trailer

https://github.com/ShangdeHan/ECS189_FinalProject

For the presskit, I mainly described what is our game about, what things are included in the game, and how to play this game and complete it. And I also added 
some side informations into the presskit to make the game sounds more interesting.
For the trailer, I picked some short clips from each level to show players what are the differences between the original version and ours version. Also, the players can see what the main screen looks like through the short videos.


## Game Feel (Name: Shangde Han)

### Summary:
Game feel in this game motivates players to explore every new things and skills to arrive the next level. 
If players do not check the pause menu, they do not know how to jump higher and how many levels in total. Like Super Mario or many other game, players need to try many different 
keys combo to discover that they can control character to hang on the wall corner. Of course, if people do not want to try many times or they would like to learn how to operate
the character directly, they can read the "README.md" before they play the game to see all tips. If people forget to check that file, they can also can some tips in the game by entering "Esc" or clicking "Pause" to know informations. Besides, it is possible that players get stuck on the specific level and cannot pass it. So, we put each levels' walkthrough to help people to know how to get the next level. However, if people would like to try everything by themselves, they will obtain a lot of sense of achievement in the process of exploring until pass all levels.       

### Game feel about frame rate:  
We spent a lot of time on pursuing a comfortable frame rate to support a better game feel. In the beginning of designing this game, we tried to use Update() function to control Robbie's movement. But we found that the character cannot move smoothly expecially after we click the jump button. Then, we found that the problem might be the difference of "GetButtonDown" and "GetButton". We checked the unity manual it shows that "GetButtonDown" Returns true during the frame the user pressed down the virtual button identified by buttonName. people need to call this function from the Update function, since the state gets reset each frame. It will not return true until the user has released the key and pressed it again. But "GetButton" Returns true while the virtual button identified by buttonName is held down. So, we separeted them to two different situations for jump. We used "GetButtonDown" to check whether the player clikc the specific button, and used "GetButton" to check whether the button is pressed. And in the end we fixed this probelm.  
However, we did not satisfied with the frame rate because sometimes it drop frames. Then, we added another function called "FixedUpdate()" to check the movement case. After improving the performance of this game, we finally feel that player can feel better when they play this game.   

### Game feel about response time / Real Time Control:  
The response time is important to measure a game. In this Robbie platform which is a level based advanture game, we focused on the players feedback. After completing the first game version, we introduced this game to other students(five people) to get their feedback and suggestions. In the process of they play the game, we noticed that the player can pay their all attention on this game to explore how to pass the current level. And they felt interested in this game, we can see that they feel happy obviously on their face when they pass one level after many times attempts. When they got stuck on some places we can see they considered a lot and think deeply to find other methods. Thus, I believe that people have a great response for this game.   

### Simulated space:   
There are three levels in this game, and each level contains axe, spike, fall stone, orb, and door to make the game be more playable. The first level is the easiest because the main purpose for this level is to let player familiar with how to operate the character to move, jump, hang on, and collect orbs to open the door. The next level is more difficult because it tests player's timing and skill in a high levle. We considered that we only desgin these two levels, but other tester students said that player will want to explore more and overcome more challenges. So, we designed the third level which is the evil difficulty for me. I failed many times in the third level, but obtained the best feeling after passing it. Therefore, based on these three levels, people will enjoy this game.   

### Polish:    
1. I added "Pause" menu when player wants to pasue the game. Also, we set a "Resume" button in that manu to let player continue the game.
2. I added "Quit" button let player quit the game when they play in the .exe file.    
3. I added a "Music Volume" slider in the pause menu to let player control the background volume. In many tests, we considered to delete the windstone sound.  
4. I added tips in the pause menu to support some operation informations, such as how to move, how to jump, how to jump higher, and how many levels in total. 
5. I improves the hang on status. In that status, player can drop off by using "Ctrl".
6. I impelmented a particle effect when Robbie is collecting orbs.
7. we fixed the third level bug that sometimes Robbie can get stuck in the wall.
8. we designed a key(Esc) command to let user Pause the game and show the "Pause" menu by clicking that key which is easier to users.
9. we changed the success image which is more relative to this game after passing all levels. 
10. We considered to have 2 different kinds of big jumps, and players are able to alter each one, but we think it is too easy for player to perform a big jump with a single button. So, we remain it as the original design("Ctrl" and "Space" combination). 
