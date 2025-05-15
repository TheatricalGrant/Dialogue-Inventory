# Dialogue-Inventory
A simple dialogue and inventory system.

# How to test the feature
You can use left mouse click on the NPC to start the dialogue, and keep left clicking to talk through the dialogue.

You can click on the item on the ground to pick it up, and I or ESC to look at your inventory. Same to close it.

# Design Decisions - Inventory
I was not able to complete all the tasks of this.
My design with how it is in the current iteration, you are able to add to your inventory, and open/close. This is through just one inventory widget.
In order to add in better functionality and make it easier on oneself to add more spots. I'd prefer a loop approach and dynamically add in a slot widget.
This would mean you could increase or decrease the slots dynamically, and use each spot for drag & drop. I just was not able to get it done in the time I had.
It also means I could just set the spots at first by looping to see which space is free, and add it dynamically that way. While keeping track of which spots are full.

For the items I went with a struct that keeps track of the name of the item if you wanted to display it, the texture for 2D objects, a mesh for 3D, and a bool to check if its 2D or not.
With this approach, you can the one struct and use it for both 2D and 3D items, by just merely changing the values. When you put it into the viewport it would check if it's 2D and show accordingly. 


# Design Decisions - Dialogue
I made a dialogue widget that takes in an array of text from the NPC you click on. 
This is to ensure you can 1. talk to them multiple times, and 2. reuse the widget throughout for any dialogue.
If this were worked on more/more fleshed out, I would want it to come from a file that can change for different languages.
Along with options to change the path of the dialogue. 