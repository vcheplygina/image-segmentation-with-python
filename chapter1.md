---
title: Chapter 1
description: >-
  Test


---
## Displaying an image and its ground truth segmentation

```yaml
type: NormalExercise
lang: python
xp: 100
skills: 2
key: 2b2c90da6a
```



`@instructions`


`@hint`


`@pre_exercise_code`
```{python}
import numpy as np
from scipy import ndimage
from scipy import misc
import matplotlib.pyplot as plt

#Load image
im = misc.imread('OAS1_0001_MR1_slice.png')
im = im/im.max()                                #Perhaps this can be done during imread already?

#Load ground truth
gt = misc.imread('OAS1_0001_MR1_binary.png')
```
`@sample_code`
```{python}
#Create a plot
f, (ax1, ax2) = plt.subplots(nrows=1, ncols=2) 

#Show image in plot 1
ax1.imshow(im,cmap=plt.cm.gray)

#Show ground truth in plot 2


#Display image
plt.show()
```
`@solution`
```{python}
#Create a plot
f, (ax1, ax2) = plt.subplots(nrows=1, ncols=2) 

#Show image in plot 1
ax1.imshow(im,cmap=plt.cm.gray)

#Show ground truth in plot two
ax2.imshow(gt,cmap=plt.cm.gray)

#Display image
plt.show()
```





