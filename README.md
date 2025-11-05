# OPENING--AND-CLOSING
### REG NO:212223240068
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:

### Step1:
Import the necessary packages

### Step2:
Give the input text using cv2.putText()

### Step3:
Perform opening operation and display the result

### Step4:
Similarly, perform closing operation and display the result

## Program:

```

# Import the necessary packages

import cv2
import numpy as np
import matplotlib.pyplot as plt
image = np.zeros((500, 500, 3), dtype=np.uint8)

# Create the Text using cv2.putText

font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'KARUNIYA M', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)


# Create the structuring element

kernel = np.ones((3, 3), np.uint8)

# Display the input image

plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')


# Use Opening operation

opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Opening Operation")
plt.axis('off')



# Use Closing Operation

closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
plt.imshow(cv2.cvtColor(closed_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Closing Operation")
plt.axis('off')
plt.show()



```
## Output:

### Display the input Image

<img width="505" height="508" alt="image" src="https://github.com/user-attachments/assets/1c592bf6-1920-4398-a716-b881fb6a8967" />


### Display the result of Opening

<img width="488" height="514" alt="image" src="https://github.com/user-attachments/assets/d9d0c9d3-827a-4e00-ab73-4ceb88d4ebf1" />


### Display the result of Closing

<img width="466" height="526" alt="image" src="https://github.com/user-attachments/assets/263481c5-d11c-4b42-a749-c51dbb3c0ad4" />



## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
