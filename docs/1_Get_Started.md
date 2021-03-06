# Get Started with Minecraft Pi Edition & Python

![UTC Logo](images/UTC_Logo.png)

# First Steps

1. Open up the "mcpi_ideas" folder on the Desktop
2. Double click on "1_Get_Started.py" and Python (IDLE) will open.
3. Open up Minecraft
    * Click on "Menu" icon in the top or bottom left of the screen ( it's usually one of these ![Menu Icon Pixel](images/launch.png) or ![Menu Icon Pi-Top](images/my-computer.png)) 
    * Then "Games" (![Games Icon Pixel](images/applications-games2.png) or ![Games Icon Pi-Top](images/applications-games.png))-> "Minecraft" ![Minecraft Icon](images/minecraft-pi-32.png))
    * Click "Start Game" -> "Create World"
    * Don't full-screen Minecraft (the mouse pointer will go funny)


# Move about a bit

* Once in Minecraft make sure you know how to get about
* A S W D
* Space bar to jump / fly
* Mouse to look, mouse buttons to build blocks and destroy them.
* ESC to get your mouse back and get out of the Minecraft 


# Run your first code

1. Move the windows around so you can see this guide, IDLE and Minecraft
2. Press ESC & click back into python editor ( IDLE )
3. Press F5 to run the code
4. You may need to click the "Save then run" or press Enter
5. Quickly click back into Minecraft to see what happens.
6. Clicking on the Minecraft window entry in the menu bar at the top can help.


# Did you see it?

If not try one more time yourself. And then wave for assistance.

# Well done

You have run your first program that manipulates Minecraft


# The Code Explained 1/3

```python
from mcpi import minecraft
from mcpi import block

# Store the connection to Minecraft in a variable called mc
mc = minecraft.Minecraft.create()
```

Get the code that allows the python programming language to talk to Minecraft.

And create the connection, you have to be in a world in Minecraft for this to work
 
# The Code Explained 2/3

```python
# Store the position player is standing in a variable called pos 
pos = mc.player.getTilePos() 
```
Python asks Minecraft what tile the player is standing on

\# means a line is a comment in English and is not part of the program.
 We use them to explain what is going on in the code.



# The Code Explained 3/3

```python
# Store a string which contains the x,y,z of your position
message = "You are at x="+str(pos.x)+", y="+str(pos.y)+", z="+str(pos.z)

# Print the message in the python screen
print(message)

# Send the message to the Minecraft chat
mc.postToChat(message)

# A quicker way to print the position
message2 = "You are at "+str(pos)
print(message2)
```



# Make some blocks
Below your current code type

```python
mc.setBlock(pos, block.DIAMOND_BLOCK)

above = pos
above.y = above.y + 4
mc.setBlock(above, block.TNT.id, 1)
```

* Run it with F5
* Look above you and below, can you see some new blocks?
* You can get a list of the blocks by typing "block." and then press CTRL + SPACE
* Experiment making different blocks and changing how far away they are


# I'm walking on sunshine

Add this code below what you have already written

What does it do when you run it?

```python
while True:
	pos = mc.player.getTilePos() 
	mc.setBlock(pos, block.GOLD_BLOCK)
```

What happened?


# Moving on

Well done. Now delete these lines from our code so we can get on .

```python
mc.setBlock(pos, block.DIAMOND_BLOCK)

above = pos
above.y = above.y + 4
mc.setBlock(above, block.TNT.id, 1)
while True:
	pos = mc.player.getTilePos() 
	mc.setBlock(pos, block.GOLD_BLOCK)
```



# Rainbow Road

Now add this piece of code

```python
while True:
  pos = mc.player.getTilePos() 
  num = (pox.x+pos.y+pos.z) % 16
  mc.setBlock(pos, block.WOOL.id, num)
```

* There is a mistake in this on purpose.
* It will appear in red in the Python window.
* See if you can see what the problem is and fix it.
* Once it works can you work out what the code is doing?

# Well done you have completed this bit



