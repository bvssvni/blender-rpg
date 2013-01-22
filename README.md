blender-rpg
===========

A simple RPG/Adventure prototyping engine for Blender (under work)  
BSD license.  

To run this you need to install ![Blender](http://www.blender.org/)   

Open it in Blender and go to Game -> Start Game Engine.  
Control the character movement with W, A, S, D.  

TODO:

1. Create a Magica, Health and Stamina bar.  
2. Make Player loose health when getting close zombies.  
3. Add a way to kill zombies. Suggestions:
3.1. Trick them into holes.
3.2. Shoot magic bullets.
3.3. Hit them with a sword.
4. Add a gate that opens when all enemies are killed.

##Zombies

When nearer that 5 units from the player, they starts walking toward it.  

When they get closer than 1 unit from the player, the player starts loosing life.  

When they get farther than 10 units, they forget the player, but continues to walk in same direction.

##Running Python Scripts

The sensor 'Delay' with 'Repeat' set to true sends a pulse for each update.  
This can be connected to a controller that runs a Python script.  
Remember to add ".py" to your script, and set the type to "Module".  
Write the name of the script without the extension, add a dot and the function to call.  
For example:

    follow_strict.main

It is a good idea to write Python scripts to behave like AND gates by default.  
This way, one can interrupt the behavior using other sensors.
Here is an example that copies the world position of the owner of controller to the owner of actuators:

    import bge

    def main(cont)
        own = cont.owner
    
        # Behave like an AND gate.
        positive = False
        for sens in cont.sensors:
            positive = positive and sens.positive
    
        # Copy position to actuator owners.
        if sens.positive:
            for act in cont.actuators:
                act.owner.worldPosition = own.worldPosition
    
On Mac, start Blender from the Terminal to get the output from "print" statements.  

    cd ../../Applications/blender.app/Contents/MacOS
    ./blender
    
Some useful functions for debugging:

    dir(obj)    Prints out functions and properties of object or module.
    
    print(msg)  Prints out a message to the console.
    
