# BrainHack DSTA 
## Easy Challenges
- ### Challenge 1 : Caesar Cipher
![Challenge 1!](../../../CTFs/assets/brainhack-writeup-stuff/challenge1.png "Challenge 1")

The first challenge was to decrypt the ciphertext. The best guess for the cipher would be Caesar cipher, based on the title. The ciphertext can then be decrypted using any online decoder. 

- ### Challenge 2 : Monoalphabetic Substituition Cipher
![Challenge 2!](../../../CTFs/assets/brainhack-writeup-stuff/crypto2qn.png "Challenge 2")

The next challenge required some research into what the cipher was. https://www.boxentriq.com/code-breaking/cipher-identifier is a good site to detect the cipher used based on the ciphertext. The plaintext was a quote from a Sherlock Holmes book, which wasn't the flag. The capital letters in the ciphertext indicated which letters from the plaintext formed the flag.

- ### Challenge 3 : Sherlock Holmes Dancing Men Cipher
![Challenge 3!](../../../CTFs/assets/brainhack-writeup-stuff/crypto3qn.png "Challenge 3")

The previous challenge provided a big clue for this challenge. We recognized the image provided in the question to be from the book the plaintext came from in challenge 2. Googling the Dancing Men cipher and putting the pieces together was fun.
