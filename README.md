# RockLobster_Internship

## Entrance assignment

Create a 5 minute gameplay video using the 3D Gamekit Lite (https://assetstore.unity.com/packages/templates/tutorials/3d-game-kit-lite-135162)

<b>Submission:</b> 5 minute gameplay video clip and a Continuous_Notes.md file displaying my progressive work, how I went about it, and if any roadblocks were hit. 

## Assignment 1

<b>End Goal:</b> Like in God of War, when Kratos gets close to a door, theres a seamless animation between the character and the door opening into a cutscene. We don't want any pauses between this interaction, the cutscene must happen as soon as the player is in a trigger area and when the cutscene ends, the game will go on as normal.

make a character in CC4 and see how it works, use that character in the Unity project provided by the supervisor make it work by using a character controller. <br>
Character controller asset: Malbers (https://malbersanimations.gitbook.io/animal-controller)

Learning steps to take up in order:

- Input mechanic of the character. 
- movement calculator.
- animator trigger.

set triggers
control taken away when entered
simulate animation

### Sub - Assignment

Understand how Scriptable objects work <br>
Reference Video - https://www.youtube.com/watch?v=raQ3iHhE_Kk

How to approach a game:

- Modular
    - Systems are not directly dependant on each other, example: inventory systems would want to communicate with other systems but we should not hard code/ hard reference the 2 systems, this will cause it to be less flexible to create other new things.

    - Scenes are clean slates - You have no transient data between scenes, every time a new scene starts it should be a clean break and load. This allows scenes to have unique behavior.

    - Prefabs - Goes hand in hand with scenes being clean slates, the prefabs should act as lego bricks that can work on their own. This helps a lot when working in groups or teams so that people don't need to go back and forth with each other when coming across a scene created object. Prefabs cannot be edited unless unpacked.

    - Components - Unity is a components based engine and components are its biggest strength. Break things up into components so that each component can work on things uniquely and differently, the next step is to make the components communicate with each other.

- Editable (Inspector section in Unity)
    - Focus on data - Making our game data driven and the Unity that process that data as instructions, it makes things easier to changes to the game.This also allows us to make changes to the game without changing the code already written.

    - Ensure that you do not need to change the code for the game unless required, this makes it easier to work with designers and artist when in teams. Otherwise, it also helps when keeping things in one place, you can edit things from the component itself to fit your needs.

    - Emergent Design - After fixing the game components together, we can actually make these components communicate with each other in such a way that new game mechanics or game features are created. This is why the word 'emergent' is used, we can add features that we didn't really expect to work out or add into the game.

    - Change at runtime - It is useful if there is a long duration in the scene, if you can change a state during runtime it can makes things simpler and easier to balance out.

- Debuggable
    - The more modular the game is, the easier it is to debug any single poece (prefabs or components).
    -  The more editor features you have on the component will make it easier to debug the issue since you don't need to go back to the code to change whatever you wanted to. Make it easier by making sure that you can see the debug state in your editor itself.
    - Do not fix a bug that You Don't Understand <b>(Important)</b> - Go through documentation, youtube videos, etc. or any other references but understand the bug that is being created, why it's there and what it's causing. After understanding it then only fix it.
    