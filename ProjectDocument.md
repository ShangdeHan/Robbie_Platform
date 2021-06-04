# Game Basic Information #

## Summary ##

**A paragraph-length pitch for your game.**

## Gameplay Explanation ##

**In this section, explain how the game should be played. Treat this as a manual within a game. It is encouraged to explain the button mappings and the most optimal gameplay strategy.**


**If you did work that should be factored in to your grade that does not fit easily into the proscribed roles, add it here! Please include links to resources and descriptions of game-related material that does not fit into roles here.**

# Main Roles #

Your goal is to relate the work of your role and sub-role in terms of the content of the course. Please look at the role sections below for specific instructions for each role.

Below is a template for you to highlight items of your work. These provide the evidence needed for your work to be evaluated. Try to have at least 4 such descriptions. They will be assessed on the quality of the underlying system and how they are linked to course content. 

*Short Description* - Long description of your work item that includes how it is relevant to topics discussed in class. [link to evidence in your repository](https://github.com/dr-jam/ECS189L/edit/project-description/ProjectDocumentTemplate.md)

Here is an example:  
*Procedural Terrain* - The background of the game consists of procedurally-generated terrain that is produced with Perlin noise. This terrain can be modified by the game at run-time via a call to its script methods. The intent is to allow the player to modify the terrain. This system is based on the component design pattern and the procedural content generation portions of the course. [The PCG terrain generation script](https://github.com/dr-jam/CameraControlExercise/blob/513b927e87fc686fe627bf7d4ff6ff841cf34e9f/Obscura/Assets/Scripts/TerrainGenerator.cs#L6).

You should replay any **bold text** with your relevant information. Liberally use the template when necessary and appropriate.

## User Interface (Name: Shangde Han)

**Describe your user interface and how it relates to gameplay. This can be done via the template.**

## Movement/Physics

**Describe the basics of movement and physics in your game. Is it the standard physics model? What did you change or modify? Did you make your movement scripts that do not use the physics system?**

## Animation and Visuals

**List your assets including their sources and licenses.**

**Describe how your work intersects with game feel, graphic design, and world-building. Include your visual style guide if one exists.**

## Input

**Describe the default input configuration.**

**Add an entry for each platform or input style your project supports.**

## Game Logic

**Document what game states and game data you managed and what design patterns you used to complete your task.**

# Sub-Roles

## Audio

**List your assets including their sources and licenses.**

**Describe the implementation of your audio system.**

**Document the sound style.** 

## Gameplay Testing

**Add a link to the full results of your gameplay tests.**

**Summarize the key findings from your gameplay tests.**

## Narrative Design

**Document how the narrative is present in the game via assets, gameplay systems, and gameplay.** 

## Press Kit and Trailer

**Include links to your presskit materials and trailer.**

**Describe how you showcased your work. How did you choose what to show in the trailer? Why did you choose your screenshots?**



## Game Feel (Name: Shangde Han)

**Document what you added to and how you tweaked your game to improve its game feel.**
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

### simulated space:   
There are three levels in this game, and each level contains axe, spike, fall stone, orb, and door to make the game be more playable. The first level is the easiest because the main purpose for this level is to let player familiar with how to operate the character to move, jump, hang on, and collect orbs to open the door. The next level is more difficult because it tests player's timing and skill in a high levle. We considered that we only desgin these two levels, but other tester students said that player will want to explore more and overcome more challenges. So, we designed the third level which is the evil difficulty for me. I failed many times in the third level, but obtained the best feeling after passing it. Therefore, based on these three levels, people will enjoy this game.   

### polish:  
1. We considered to have 2 different kinds of big jumps, and players are able to alter each one, but we think it is too easy for player to perform a big jump with a single button. So, we remain it as the original design("Ctrl" and "Space" combination).   
2. We added "Pause" menu when player wants to pasue the game. Also, we set a "Resume" button in that manu to let player continue the game.
3. We added "Quit" button let player quit the game when they play in the .exe file.   
4. 
