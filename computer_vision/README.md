# 
# Computer Vision Challenge

## Dataset
**Company X's** [Ad Campaign Creatives](https://drive.google.com/drive/folders/1La9Vvn4CI5Sz98DjvbZbHvPGOGin7hSC?usp=sharing) comprises  of creatives from different brands. 



## Tasks

## Task 1 - 40 Points
### Identity  and Segment all the artifacts

There are different types of artifacts in these creative.  This tasks revolves around segmenting majorly two different sets of them, one being any text block,  be it header, trademarks, etc. Apart from text blocks there are usually products/objects, and models present on the creative. You can ignore all the products/objects. The second set comprises of people/models present on these ad creatives. The final output from this step will be a set of binary masks that defines the background and these set of artifacts.

` Some of the objects classes might not be available in most of the pre-trained object segmentation models available online as they are trained on limited subset of objects using datasets like COCO or  Object365. So please ignore those objects for this task.`


## Task 2 - 40 Points
### Impaint  and remove the Identified artifacts
 
**Image Inpainting** is a task of reconstructing missing regions in an image. Using the generated masks from the previous steps, remove the artefacts from the creatives and  use [Resolution-robust Large Mask Inpainting with Fourier Convolutions](https://saic-mdal.github.io/lama-project/)  to fill in the removed artifacts. This would a generate a much consistent background. The output from this step will be a set of  artifacts identified in the last step, and a background for each example creative present in the test set.



## Task 3 - 20 Points
### Research/Learning

Summarise your learnings and work as well as suggest an alternative approach to do end to end segmentation and impainting. Also for this task, you didn’t train your own segmentation network, but in creatives, they might have different products that might not be in the objects subset that you trained the segmentation/object detection model on.  How would you tackle these edge cases. 

![tasks](https://github.com/MaayaLabs/internship_challenges/blob/main/computer_vision/img/impainting.png?raw=true)
