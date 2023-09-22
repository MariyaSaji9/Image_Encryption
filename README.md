# About
Image encryption is the process of converting an image into a scrambled, unreadable form that can 
only be decrypted and viewed by someone with the appropriate decryption key. This is often done to 
protect sensitive or personal information contained in an image, such as a person's face or a company's 
logo. This project is a confusion-diffusion-based image encryption technique that depends on a well-known chaotic map called the
Henon map and the deep Convolutional Neural Network (CNN).
***
# Project overview
The project have two phases,  In the first phase, the CNN model is used for feature extraction and the extracted feature can be used to 
generate the key. Then the key will be used as the initial values and the control parameters for the 
chaotic map to generate the chaotic sequences, which will be used in the second phase. The second 
phase, the encryption phase, mainly includes pixel confusion Using Hilbert Curve and diffusion using 
the XOR operation.XOR operation is performed on the original, mask, and previous ciphered pixels.
The Binary of the ciphered pixel is shifted for producing the encrypted image.
### 1. Key Generation
The generation of keys via a deep CNN model 
by employing VGG16 architecture with the pre-trained network having an Image-Net dataset with 
1000 categories.
### 2. Mask image generation
In the proposed encryption technique sequences are generated using a high-dimensional chaotic 
map called the Henon map. After all operations a mask image is generated.
### 3. Scrambling
pixel scrambling using Hilbert Curve.
### 4. Diffusion and Encryption
Diffusion refers to changing the individual pixel grey values that reduce the correlation between 
image pixels. In the diffusion stage, pixel values are modified to confuse the relationship between the 
cipher and plain images. The pixels of the image from “The Henon map (T), scrambled image (I), and 
the previous ciphered pixel (𝐶𝑝) are given to an XOR operation to obtain the pixels of the encrypted 
image (C).
𝐶 = [𝐼 ⊕ 𝑇] ⊕ 𝐶𝑝
After the XOR operation, the binary of each ciphered pixel is shifted for better encryption. As a result 
of XOR operation and shifting the encrypted image is obtained.
# Performance analysis
The correlation coefficient value of the encrypted image is near 0 and negative. The 
net pixel change rate (NPCR) value is greater than 99%. The unified average changing intensity 
(UACI) value is near 33.33. The key space is near 2<sup>100</sup>.


