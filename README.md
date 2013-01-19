blender-rpg
===========

A simple RPG/Adventure prototyping engine for Blender (under work)  
BSD license.  

To run this you need to install ![Blender](http://www.blender.org/)   

Open it in Blender and go to Game -> Start Game Engine.  
Control the character movement with W, A, S, D.  

TODO:

1. Create a Magica, Health and Stamina bar.  
2. Add one object for Enemy, Item and Gate.  
3. Make the camera follow the character.  
4. Add mouse cursor to click and interact with objects.

##Zombies

When nearer that 5 units from the player, they starts walking toward it.  

When they get closer than 1 unit from the player, the player starts loosing life.  

When they get farther than 10 units, they forget the player, but continues to walk in same direction.

