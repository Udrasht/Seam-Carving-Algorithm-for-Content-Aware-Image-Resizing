# Image_Resizing
Image Resizing using Seam Carving Algorithm

## Problem Statement: 
Apply seam carving content aware image-resizing algorithm on a given image. Take the height and width (in pixels) of the output image as inputs from the user.

### What is Seam Carving?
- Seam-carving is a content-aware image resizing technique where the image is reduced in size by one pixel of height (or width) at a time.
- A vertical seam in an image is a path of pixels connected from the top to the bottom with one pixel in each row.
- A horizontal seam is a path of pixels connected from the left to the right with one pixel in each column.
- Steps:
    - Energy Calculation: Each pixel has some RGB values.
    Calculate energy for each pixel. For ex.- You can use
    dual-gradient energy function but you are free to use any
    energy function of your choice. Also, you can refer to this
    [link](https://www.cs.princeton.edu/courses/archive/fall17/cos226/assignments/seam/index.html) for details.
    - Seam Identification: Identify the lowest energy seam.
    - Seam Removal: Remove the lowest energy seam.
### Program Flow:
  - Extract individual pixel’s RGB values from the sample image
    ./data/input/sample.jpeg and write them into ./data/input/rgb_in.txt
  - Load the RGB values from ./data/input/rgb_in.txt in a 3D matrix.
  - Apply seam carving algorithm.
  - Write the individual pixel’s RGB values for resized image into the
    ./data/output/rgb_out.txt
  - Generate sample image output ./data/output/sample_out.jpeg
    using the ./data/output/rgb_out.txt.
### Dependencies:
- You’ll need to install the python image library Pillow to extract RGB
values of each pixel and to generate images back from RGB values of
each pixel.
- To install Pillow: pip install Pillow

**The python script is only compatible with Linux/Mac operating systems.**

### How to Run::
- ```python3 driver.py <input_mage_name>```
- Ex:  ```python3 driver.py sample1.jpeg```
---
### Output Example

- #### Sample Image1
  Original Image
  
   ![Image 1](/data/input/sample4.jpeg)
  
  Resized Image
  
   ![Image 2](/data/output/sample_out4.jpeg)
  
- #### Sample Image2
  Original Image
  
   ![Image 3](/data/input/sample1.jpeg)
  
  Resized Image
  
  ![Image 4](/data/output/sample_out1.jpeg)
  
- #### Sample Image3
  Original Image
  
   ![Image 5](/data/input/sample3.jpeg)
  
  Resized Image
  
   ![Image 6](/data/output/sample_out3.jpeg)



