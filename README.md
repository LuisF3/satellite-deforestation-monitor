### [Overview](#overview) | [Students](#students) | [Examples](#examples) | [Results](#results)  | [References](#references) 

# Satellite-deforestation-monitor

This is the final project for the image processing course at the University of São Paulo (USP)
Este é 


---
### Overview
In this project we did a simple system for deforestation monitoring.

In order to do this we did the following steps:
 - First we apply a Gaussian low-pass filter in order to smooth the image, which results in a blured image.
 - The target image is converted to the HLS model
 - The image is binarized following the following criteria :
   - The value 1 is assigned to all regions with hue between 110 and 200 (considering a hue in the range 0-360), which represents the green color, and luminance less than about 25%, which represents dark colors. That is, the value 1 is assigned to all dark green pixels.
   - The value 0 is assigned to other pixels
 - An opening operation is applied to reduce isolated areas that are dark green.
 - A closing operation is performed to unify regions with many dark green pixels but with 'holes'.
 - Apply a filter by regions with high variance (ideally because they are regions with foliage).
 - Apply a histogram-based segmentation techniques
 - Removal of regions with areas smaller than a certain noise removal threshold

--- 
### Examples
Please see the following tutorial notebooks for a guide on how to use **satellite-deforestation-monitor** on your projects:
 - **How to use** : [Introduction](https://drive.google.com/drive/folders/1mP4s86rJRre1cNfXYY7-XOkVATl5tZIn)

---
### Results
 
![alt text](https://github.com/LuisF3/satellite-deforestation-monitor/blob/main/Imagens%20before-after/examples/download%20(4).png)
  
---
### Students
  - Henrique Tadashi Tarzia - 10692210
  - Lucas Xavier Ebling Pereira - 10692183
  - Luis Felipe Ribeiro Chaves - 10801221 
  - Victor Akihito Kamada Tomita - 10692082
---

### References
 - [Satellite forest reconition](https://clouard.users.greyc.fr/Pantheon/experiments/forestarea-extraction/index-en.html)
