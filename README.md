# Steganography
 This is the project that me and my team has done for the college project. 
 Steganography hides the data in any form such as image, video, text, or audio.

# Project Name: Pixel Whispers Unveiling the Secrets of Image Steganography
 Made By - L V Manikanta Maguluri
          , M Bhaskar Raja
         , K Sree Hari Kumar Reddy 
* Steganography is the art of hiding the fact that communication is taking place, by hiding information in other information. 
* This project hides the message within the image, text, audio, and video files. In this project, the sender selects a cover file (image or text) with secret text and hides it into the cover file by using an efficient algorithm and generates a stego file of the same format as our cover file (image or  text). Then the stego file is sent to the destination with the help of private or public communication networks. On the other side i.e. receiver, the receiver downloads the stego file and by using the appropriate decoding algorithm retrieves the secret text that is hidden in the stego file.

# Image Steganography ( Hiding TEXT in IMAGE ) :
* Using ***Least Significant Bit Insertion*** we overwrite the LSB bit of actual image with the bit of text message character. At the end of the text message, we push a delimiter to the message string as a checkpoint useful in the decoding function. We encode data in order of Red, Green and then Blue pixels for the entire message.

* We get its ASCII value and it is incremented or decremented based on if ASCII value between 32 and 64 , it is incremented by 48(ASCII value for 0) it is decremented by 48
* Then xor the obtained value with 170(binary equivalent-10101010) 
* Convert the obtained number from the first two steps to its binary equivalent then add "0011" if it earlier belonged to ASCII value between 32 and 64 else add "0110" making it 12-bit for each character.
* With the final binary equivalent we also 111111111111 as a delimiter to find the end of the message 
* Now from 12 bits representing each character every 2 bits is replaced with equivalent ZWCs according to the table. Each character is hidden after a word in the cover text.

# Text Steganography ( Hiding TEXT in TEXT ) :
* In Unicode, there are specific zero-width characters (ZWC). We used four ZWCs to hide the Secret Message through the Cover Text.

