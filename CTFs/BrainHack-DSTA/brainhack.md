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
![Challenge 4!](CTFs/assets/brainhack-writeup-stuff/linux1qn.png "Challenge 4")

This challenge simply required us to connect to the server and given port number using netcat (as hinted in the description) to retrieve the flag. 

- ### Challenge 5 : Linux Integer Overflow

The big hint for this challenge was the title. It refers to the number of bits required to store the largest integer in a 32-bit system. Hence, the most probable attack to use here would be integer overflow. Sure enough entering 2147483648 gave us -2147483648 and as we started incrementing the input by 1, the negative number being output would decrease by 1. Seeing as the description talked about 0 so much. I thought the output should be 0 to get the flag. 

![Challenge 4 Flag!](CTFs/assets/brainhack-writeup-stuff/linux2flag.png) 

Inputting twice of 2147483648 would mean the output is 0, and gave us the flag.

- ### Challenge 5 : Networks - Wireshark (basic)

![Challenge 5!](CTFs/assets/brainhack-writeup-stuff/network1qn.png "Challenge 5")

This challenge required basic wireshark skills (And the knowledge that wireshark is able to capture all http objects i.e. files too)
From the pcap file, we saved all http objects and opened the file Confidential.pdf and got the flag :-))

- ### Challenge 6 : Networks - Wireshark (Slightly more work than basic)

![Challenge 6!](CTFs/assets/brainhack-writeup-stuff/network2qn.png "Challenge 6") 

This challenge required the same wireshark knowledge as the previous one, except we needed to know how to use the filter to only sieve out http/s traffic. 


