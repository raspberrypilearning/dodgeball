## Lasers!

Let's make your game a little harder to complete, by adding lasers!

--- task ---

Add a new sprite to your game, called 'Laser'. It should have 2 costumes, called 'on' and 'off'.

![screenshot](images/dodge-lasers-costume.png)

--- /task ---

--- task ---

Place your new laser anywhere you like, between 2 platforms.

![screenshot](images/dodge-lasers-position.png)

--- /task ---

--- task ---

Add code to your laser, to make it switch between the 2 costumes.

```blocks
	when flag clicked
	forever
		switch costume to [on v]
		wait (2) secs
		switch costume to [off v]
		wait (2) secs
	end
```

If you prefer, you can `wait`{:class="blockcontrol"} a `random`{:class="blockoperators"} amount of time between costume changes.

--- /task ---

--- task ---

Finally, add code to your laser, so that the 'hit' message is broadcast when the laser touches your character. 

--- hints ---

--- hint ---

This code will be very similar to the code you added to your ball sprite.

--- /hint ---


--- hint ---

Copy the code you created for the ball sprite which `broadcasts 'hit'`{:class="blockcontrol"} when it is `touching your character`{:class="blocksensing"}.

--- /hint ---

--- hint ---

This is the code you should add:

```blocks
when green flag clicked
forever 
  if <touching [Pico walking v] ?> then 
    broadcast [hit v]
  end
end
```

--- /hint ---

--- /hints ---

You don't need to add any more code to your character - it already knows what to do when it is hit!

--- /task ---

--- task ---

Test out your game to see if you can get past the laser. Change the `wait`{:class="blockcontrol"} times in your code if the lasers are too easy or too hard.

--- /task ---
