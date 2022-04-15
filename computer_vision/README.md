# 
# Computer Vision Challenge

## Dataset
**Company X's** [Ad Campaign Creatives](https://drive.google.com/drive/folders/1La9Vvn4CI5Sz98DjvbZbHvPGOGin7hSC?usp=sharing) comprises  of creatives from different brands. 



## Tasks

## Task 1 - 40 Points
### Identity  and Segment all the artifacts

There are different types of artifacts in these creatives. This task revolves around segmenting the following artifacts:
1. Text Elements:  title, headers, product descriptions, trademarks, etc.
2. Humans: humans/models present on the creative. 

The final output from this step will be a set of binary masks that differentiate these set of artifacts from the background.


## Task 2 - 40 Points
### Remove the Identified artifacts and Inpaint
 
**Image Inpainting** is a task of reconstructing missing regions in an image. Using the generated masks from the previous steps, remove the artifacts from the creatives and  use [Resolution-robust Large Mask Inpainting with Fourier Convolutions](https://saic-mdal.github.io/lama-project/)  to fill in the removed artifacts. This would help us recover the background of our creative. 

The output from this step will be as follows:
1. Artifacts identified/segmented in each creative of the test set(Follows from Task 1).
2. A background for each example creative present in the test set.

![tasks](https://github.com/MaayaLabs/internship_challenges/blob/main/computer_vision/img/impainting.png?raw=true)


## Task 3 - 20 Points
### Research/Learning

1. Summarise your learnings and work as well as suggest an alternative approach to do end to end segmentation and impainting.
2. Creatives can contain artifacts that might not be in the objects subset that you trained the segmentation/object detection model on(COCO, ImageNet etc).  How would you tackle these edge cases?

