## Character movement

Start by creating a character that can move left and right, and can climb up ladders.

--- task ---

Open the 'Dodgeball' Scratch starter project.

**Online:** open the starter project at [rpf.io/dodgeball-on](http://rpf.io/dodgeball-on). 

**Offline:** download the starter project from [rpf.io/dodgeball-off](http://rpf.io/dodgeball-off) and then open it using the offline editor.

--- /task ---

The project contains a backdrop with platforms:

![dodgeball project background](images/dodge-background.png)

--- task ---

Choose a new sprite as the character the player will control, and add it to your project. It's best if you choose a sprite with multiple costumes, so that you can make it look as though it's walking.

![pick a sprite](images/dodge-characters.png)

[[[generic-scratch-sprite-from-library]]]

--- /task ---

--- task ---

Add code blocks to your character sprite so that the player can use the arrow keys to move the character around. When the player presses the right arrow, the character should point right, move a few steps, and change to the next costume:

![pico walking sprite](images/pico_walking_sprite.png)
```blocks
when flag clicked
forever
	if <key [right arrow v] pressed? > then
		point in direction (90 v)
		move (3) steps
		next costume
	end
end
```

--- /task ---

--- task ---

Test out your character by clicking the flag and then holding down the right arrow key. Does your character move to the right? Does your character look like it is walking?

![screenshot](images/dodge-walking.png)

--- /task ---

--- task ---

Add code blocks to the character sprite's `forever`{:class="blockcontrol"} loop so that it walks left if the left arrow key is pressed.

--- hints ---

--- hint ---

So that your character can move to the left, you'll need to add another `if`{:class="blockcontrol"} block inside the `forever`{:class="blockcontrol"} loop. In this new `if`{:class="blockcontrol"} block, add code to make your character sprite `move`{:class="blockmotion"} to the left.

--- /hint ---

--- hint ---

Copy the code you created to make the character walk to the right. Then set the `key pressed`{:class="blocksensing"} to the `left arrow`{:class="blocksensing"}, and change the `direction`{:class="blockmotion"} to `-90`.

```blocks
if <key [right arrow v] pressed? > then
	point in direction (90 v)
	move (3) steps
	next costume
end
```

--- /hint ---

--- hint ---

Your code should look like this now:

![pico walking sprite](images/pico_walking_sprite.png)
```blocks
when green flag clicked
forever 
  if <key [right arrow v] pressed?> then 
    point in direction (90 v)
    move (3) steps
    next costume
  end
  if <key [left arrow v] pressed?> then 
    point in direction (-90 v)
    move (3) steps
    next costume
  end
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

Test your new code to make sure that it works. Does your character turn upside-down when walking to the left?

![screenshot](images/dodge-upside-down.png)

If so, you can fix this by clicking the `(i)`{:class="blocksensing"} icon on your character sprite, and then clicking the left-right arrow.

![screenshot](images/dodge-left-right.png)

Or if you prefer, you can also fix the problem by adding this block to the start of your character's script:

```blocks
set rotation style [left-right v]
```

--- /task ---

--- task ---

To climb a pink ladder, your character sprite should move a few steps upwards on the Stage whenever the up arrow is pressed **and** the character is touching the correct colour. 

Add inside your character's `forever`{:class="blockcontrol"} loop to `change`{:class="blockmotion"} the character's `y` (vertical) position `if`{:class="blockcontrol"} the `up arrow is pressed`{:class="blocksensing"} and the character is `touching the colour pink`{:class="blocksensing"}.

![pico walking sprite](images/pico_walking_sprite.png)

```blocks
	if < <key [up arrow v] pressed?> and <touching color [#FF69B4]?> > then
		change y by (4)
	end
```

--- /task ---

--- task ---

Test your code. Can you make the character climb the pink ladders and get to the end of the level?

![screenshot](images/dodge-test-character.png)

--- /task ---
