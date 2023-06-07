# GAME-PROGRAMMING-EXP5
# EXP 05 - AMMO COLLECTION

## AIM:

To create ammo to increase the bullet count and increase the bullet spawn count.

## ALGORITHM:

### For Adding Bullet Count:

#### STEP 1: Create a HUD Blueprint:

* In the Content Browser, right-click in the desired folder.
*  Select Create Basic Asset > Blueprint Class.
*  In the Class Settings window, search for "HUD" and select it as the parent
class. Name the Blueprint (e.g., "GameHUD") and click Create.

### STEP 2: Open the GameHUD Blueprint:

* Open the GameHUD Blueprint you just created.
* In the Blueprint editor, find the Canvas panel on the left.
* Add a Text block widget to the Canvas panel to display the bullet count.
* Position the Text block widget on the canvas as desired.

### STEP 3: Create a reference to the player character:

* In the GameHUD Blueprint, create a variable of the player character's
class to store a reference to it.
* To do this, go to the Variables panel and click the "+" button.
* Set the variable type to the class of your player character (e.g.,
ThirdPersonCharacter).
* Name the variable (e.g., PlayerCharacter).

#### STEP 4: Update the bullet count display:

* In the GameHUD Blueprint, locate the Event Tick event.
* Drag off the PlayerCharacter variable and search for "Get Bullet Count"
(assuming you have a bullet count variable in your player character
Blueprint). Connect the output of the Get Bullet Count node to the Text
block widget's Text property.
* You may need to format the bullet count value as a string before
connecting it to the Text property.

#### STEP 5: Set the GameHUD as the active HUD:

* Open your player character Blueprint.
* In the Blueprint editor, locate the Event Begin Play event.
* Drag off the execution line and search for "Create Widget".
* In the Create Widget node, select the GameHUD Blueprint you created.
*  Drag off the return value of the Create Widget node and search for "Add
To Viewport".
* Compile and save the player character Blueprint.

#### STEP 6: Test the bullet count display:

* Play the game in the editor.
* Ensure that the bullet count is displayed on the screen as you interact with
the game, such as firing bullets or picking up ammo.
