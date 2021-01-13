# steganography
this is my Repository which is based on python language which name is staganography.

# Algorithm for creating the project steganography with helps of python in jupyter notebook¶
1) First we have import Image from pillow(PIL) module.
 ## Installing pillow package is very easy, especially if    you’re installing it using pip.

 ## Installing Pillow using pip
## To install pillow using pip, just run the below command in your command prompt −
###  python - m pip install Pillow
2) Now define the function name genData(data) for convert encoding data into 8-bit binary form using ASCII value of character
3) defien the function modPix where Pixels are modified according to the 8-bit binary data and finally returned
4) define a function Encode for Encode data into image and define decode function which is Decode the image into data

# what is  steganography and how it is work.

## What is Steganography?
Steganography is the process of hiding a secret message within a larger one in such a way that someone can not know the presence or contents of the hidden message. The purpose of Steganography is to maintain secret communication between two parties. Unlike cryptography, which conceals the contents of a secret message, steganography conceals the very fact that a message is communicated. Although steganography differs from cryptography, there are many analogies between the two, and some authors classify steganography as a form of cryptography since hidden communication is a type of secret message.
## Advantage of using Steganography over Cryptography?
Up to now, cryptography has always had its ultimate role in protecting the secrecy between the sender and the intended receiver. However, nowadays steganography techniques are used increasingly besides cryptography to add more protective layers to the hidden data. The advantage of using steganography over cryptography alone is that the intended secret message does not attract attention to itself as an object of scrutiny. Plainly visible encrypted messages, no matter how unbreakable they are, arouse interest and may in themselves be incriminating in countries in which encryption is illegal. [1]
## Types of Steganography
Steganography works have been carried out on different transmission media like images, video, text, or audio.

## Least Significant Bit Steganography
We can describe a digital image as a finite set of digital values, called pixels. Pixels are the smallest individual element of an image, holding values that represent the brightness of a given color at any specific point. So we can think of an image as a matrix (or a two-dimensional array) of pixels which contains a fixed number of rows and columns.


 ## How LSB technique works?
Each pixel contains three values which are Red, Green, Blue, these values range from 0 to 255, in other words, they are 8-bit values. [4] Let’s take an example of how this technique works, suppose you want to hide the message “hi” into a 4x4 image which has the following pixel values:
[(225, 12, 99), (155, 2, 50), (99, 51, 15), (15, 55, 22),(155, 61, 87), (63, 30, 17), (1, 55, 19), (99, 81, 66),(219, 77, 91), (69, 39, 50), (18, 200, 33), (25, 54, 190)]
Using the ASCII Table, we can convert the secret message into decimal values and then into binary: 0110100 0110101.Now, we iterate over the pixel values one by one, after converting them to binary, we replace each least significant bit with that message bits sequentially (e.g 225 is 11100001, we replace the last bit, the bit in the right (1) with the first data bit (0) and so on).This will only modify the pixel values by +1 or -1 which is not noticeable at all. The resulting pixel values after performing LSBS is as shown below:
[(224, 13, 99),(154, 3, 50),(98, 50, 15),(15, 54, 23),(154, 61, 87),(63, 30, 17),(1, 55, 19),(99, 81, 66),(219, 77, 91),(69, 39, 50),(18, 200, 33),(25, 54, 190)]

