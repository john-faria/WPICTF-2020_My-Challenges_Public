Files/hosting information:
	block-gate-world.zip - zip file containing Minecraft world folder
	description-draft.txt - just some text that's a draft for the challenge description
Description:
	The folder is all of the file necessary to load a Minecraft world. It is trivial to start-up the world using the Minecraft game software. Participants will spawn into the world just as some falling water is about to destroy a complex redstone circuit. The circuit was lighting-up a series of 7-segment displays that together cycled through the different characters of the flag. The challenge can be solved in MANY different ways by exploiting Minecraft mods/cheats or by reverse-engineering the mostly-destroyed circuit (there are many clues a participant can follow, it is possible)
Category:
	Misc
Solution:
	1. Unzip the file "block-gate-world.zip"
		1.5. Make a backup of the folder (not required, but a good idea)
	2. Create a new world in the Minecraft launcher based on the unzipped world folder
	3. Watch as the circuit broadcasting the secret flag is destroyed by water and spend some time brainstorming how to get the circuit/flag
	- If you are solving via Minecraft cheats/mods:
		a. Think of a game mod that could allow you to see the circuit running (preventing redstone from being destroyed, removing the water, getting a screenshot of the circuit before it is destroyed, reversing the world file to find where the redstone is)
		b. Implement that cheat/mod and restore the world from your backup
		c. Watch the circuit run and translate the 7-segment display to the flag
	- If you are solving via reverse-engineering the destroyed circuit (this way is more difficult):
		a. Spend some time looking at the construction of the different 7-segment displays, how the power flows, etc
		b. Observe the different trails that were constructed for the redstone and the destroyed redstone components that are relatively close to where they were destroyed
		c. rebuild the circuit and figure out what the flag would be
Ranking:
	Easy
Flag:
	"WPI{02301}"
Author:
	The_Abjuri5t (John F.)

