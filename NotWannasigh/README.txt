Files/hosting information
	* 192-168-1-11_potential-malware.pcap - pcap file containing some clues about the ransomware (it actually contains the seed for key generation in one of the packets)
	* NotWannasigh.zip - encrypted zip file containing the ransomware executable, decryption password in "infected"
	* flag-gif.EnCiPhErEd - encrypted file containing the flag (the WPI{...} flag is inside the gif)
	* ransomNote.txt - just a text file that the ransomware creates
	* description-draft.txt - some text that's a draft for the challenge description
	It would be great if we could allow participants to download the first 4 files (the pcap, NotWannasigh.zip, flag-gif.EnCiPhErEd, and ransomNote.txt) from the challenge. We may have to compress all of them into one zip so that they can all be downloaded at one.
Description:
	This challenge emulates the awesome work that malware researchers/volunteers do with reverse-engineering crappy ransomware to create programs that will recover files for free. The ransomware that I wrote is very poorly written (the seed is the epoch time, I just xor the file, the seed is sent to the C&C in clear text, there are print statements detailing what's going on, etc)
Category:
	Reversing
Solution:
	1. Unzip NotWannasigh.zip, the password is "infected"
	2. Create a dummy-file named flag.gif and use a debugger to observe the program's execution
	3. Notice the seed being sent out through a socket, and locate the original seed in the pcap
	4. Watch how the key is generated using random (it generates numbers between 0-255 and assigns them to unsigned chars)
	5. Using the seed from the pcap, re-create the key of unsigned chars and xor it with flag-gif.EnCiPhErEd
	6. Open the gif and see the flag being proudly displayed
Ranking:
	Easy
Flag:
	"WPI{It_always_feels_a_little_weird_writing_malware}"
Author:
	The_Abjuri5t (John F.)
