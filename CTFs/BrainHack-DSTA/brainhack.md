# BrainHack DSTA 
## Easy Challenges
- ### Challenge 1 : Caesar Cipher
![Challenge 1!](/CTFs/assets/brainhack-writeup-stuff/challenge1.png "Challenge 1")

The first challenge was to decrypt the ciphertext. The best guess for the cipher would be Caesar cipher, based on the title. The ciphertext can then be decrypted using any online decoder. 

- ### Challenge 2 : Monoalphabetic Substituition Cipher
![Challenge 2!](/CTFs/assets/brainhack-writeup-stuff/crypto2qn.png "Challenge 2")

The next challenge required some research into what the cipher was. https://www.boxentriq.com/code-breaking/cipher-identifier is a good site to detect the cipher used based on the ciphertext. The plaintext was a quote from a Sherlock Holmes book, which wasn't the flag. The capital letters in the ciphertext indicated which letters from the plaintext formed the flag.

- ### Challenge 3 : Sherlock Holmes Dancing Men Cipher
![Challenge 3!](/CTFs/assets/brainhack-writeup-stuff/crypto3qn.png "Challenge 3")

The previous challenge provided a big clue for this challenge. We recognized the image provided in the question to be from the book the plaintext came from in challenge 2. Googling the Dancing Men cipher and putting the pieces together was fun.

- ### Challenge 4 : Linux - netcat
![Challenge 4!](/CTFs/assets/brainhack-writeup-stuff/linux1qn.png "Challenge 4")

This challenge simply required us to connect to the server and given port number using netcat (as hinted in the description) to retrieve the flag. 

- ### Challenge 5 : Linux Integer Overflow

The big hint for this challenge was the title. It refers to the number of bits required to store the largest integer in a 32-bit system. Hence, the most probable attack to use here would be integer overflow. Sure enough entering 2147483648 gave us -2147483648 and as we started incrementing the input by 1, the negative number being output would decrease by 1. Seeing as the description talked about 0 so much. I thought the output should be 0 to get the flag. 

![Challenge 4 Flag!](/CTFs/assets/brainhack-writeup-stuff/linux2flag.png) 

Inputting twice of 2147483648 would mean the output is 0, and gave us the flag.

- ### Challenge 5 : Networks - Wireshark (basic)

![Challenge 5!](/CTFs/assets/brainhack-writeup-stuff/network1qn.png "Challenge 5")

This challenge required basic wireshark skills (And the knowledge that wireshark is able to capture all http objects i.e. files too)
From the pcap file, we saved all http objects and opened the file Confidential.pdf and got the flag :-))

- ### Challenge 6 : Networks - Wireshark (Slightly more work than basic)

![Challenge 6!](/CTFs/assets/brainhack-writeup-stuff/network2qn.png "Challenge 6") 

This challenge required the same wireshark knowledge as the previous one, except we needed to know how to use the filter to only sieve out http/s traffic. 

- ### Challenge 7 : Web - Page Source

 ![Challenge 7!](/CTFs/assets/brainhack-writeup-stuff/webquestion.png "Challenge 7")

 The first web challenge was very basic. Go to the website, open up the page source and look for the flag . 

![Challenge 7 Website!](/CTFs/assets/brainhack-writeup-stuff/webpage.png "Challenge 7 Website")

![Challenge 7 Flag!](/CTFs/assets/brainhack-writeup-stuff/webflag.png "Challenge 7 flag")

- ### Challenge 8 : Web - Scripts

![Challenge 8!](/CTFs/assets/brainhack-writeup-stuff/web2qn.png "Challenge 8")

The challenge description provided the hint that something is wrong with the login. Hence we should look at the script for login. 

![Challenge 8 page source!](/CTFs/assets/brainhack-writeup-stuff/web2source.png "Challenge 8 page source")

Sure enough the source had the flag but, it had to be decoded using md5 hash.

![Challenge 8 flag!](/CTFs/assets/brainhack-writeup-stuff/web2flag.png "Challenge 8 flag")

- ### Challenge 9 : Web - HTTP Requests

![Challenge 9!](/CTFs/assets/brainhack-writeup-stuff/web3qn.png "Challenge 9")

This was a slightly harder challenge. The title and description hint towards sending a POST request, which was confirmed in the webpage. 

![Challenge 9 webpage!](/CTFs/assets/brainhack-writeup-stuff/web3source.png "Challenge 9 webpage")

So on very deep inspection of the HTTP headers we realized and after a hint from sending a post request - "You are not authorized!" , We realized we had to send an authorization header. The current authorization header was "No" in base64. So we sent a POST request + an authorization header with "Yes" in base64 and retrieved the flag :))

![Challenge 9 flag!](/CTFs/assets/brainhack-writeup-stuff/web3flag.png "Challenge 9 flag")

- ### Challenge 10 : Windows - Decompiling Python Program

![Challenge 10!](/CTFs/assets/brainhack-writeup-stuff/windows1qn.png "Challenge 10")

This challenge was quite straightforward. The title suggests we needed to decompile the exe file and the description suggests that py2exe was used to create the exe file. A quick google search showed us a github tool we could use to decompile exe files that were compiled with py2exe. The python code contained the flag!






