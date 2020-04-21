Files/hosting information:
	invoice.zip - password protected zip file containing sorta-malicious JS code, and an obfuscated flag
	description-draft.txt - just some text that's a draft for the challenge description
Description:
	The file is an html document that executes some basic javascript. The two main parts of the javascript code are a seriously obfuscated string that used to be a hidden url, and some infinite popup-generating loop that will crash most webbrowsers. The challenge can be solved by analyzing the instructions to manually calculate the string, or by commenting-out the malicious lines of code and using a javascript debugger like FireBug to view the string.
Category:
	Reversing
Solution:
	1. Move the file over to a VM (we practice safe analysis here) and unzip it using the password "I_understand_that_this_challenge_contains_LIVE_MALWARE"
	2. Use a code-beautifier to unpack all of the "pro-coded" javascript - make it all on individual lines + indented properly
	3. Spend some time understanding what the code does and how it works
	- If you are solving via dynamic analysis:
		a. Prevent the infinite for-loop by commenting it out
		b. Stop the endless storm of popups by commenting those lines out, or just dissabling popups in your VM's webbrowser (or better yet, do both)
		c. Assign the mess of concatenated arrays and function calls to a new variable and print-out that variable (can also just view the variable being passed to the function call using a js-debugger like FireBug)
	- If you are solving via looking at the code:
		a. Start by researching and understanding the validity of the strange array concatenations and function declarations
		b. Begin translating the construction of the various arrays and the final call to all of the smaller strings (Notepad++ has been successfully used to help understand the array calls and accomplish this)
	Participants may start with the second solution before getting a solid understanding of the code and realizing that they can just do the first
	(both of these solutions have been tested and do work)
Ranking:
	Medium - considering making it hard because this challenge is marked as dangerous and can crash your webbrowser if you're being stupid
Flag:
	"WPI{Oh_nose_procoding_detected}"
Author:
	The_Abjuri5t (John F.), who did infact plagiarize the code from an anonymous phisher
