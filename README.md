blender-rpg
===========

A simple RPG/Adventure prototyping engine for Blender (under work)  
BSD license.  

To run this you need to install ![Blender](http://www.blender.org/)   

Open it in Blender and go to Game -> Start Game Engine.  
Control the character movement with W, A, S, D.  

TODO:

1. Create a Magica, ~~Health~~ and Stamina bar.  
2. ~~Make Player loose health when getting close to zombies.~~  
2.1. ~~Make level restart when all health is lost.~~  
3. Add a way to kill zombies. Suggestions:  
3.1. ~~Trick them into holes.~~  
3.1.1. Make zombies disappear when colliding with the fall off plane.  
3.2. Shoot magic bullets.  
3.2.1. This might be possible with the "Edit Object" actuator.  
3.3. Hit them with a sword.  
4. Add a gate that opens when all enemies are killed.  
4.1. Alternative: Load 2nd level.  
4.2. Either add an enemy counter (Python script) which decreases when they die,  
4.3. or, when there is no enemies nearby in a large radius from player.  

##Zombies

When nearer that 5 units from the player, they starts walking toward it.  

When they get closer than 1 unit from the player, the player starts loosing life.  

When they get farther than 10 units, they forget the player, but continues to walk in same direction.

##Python Scripts

Scripts are tested and written in a separete repository ![blender-bge-scripts](https://github.com/bvssvni/blender-bge-scripts)


