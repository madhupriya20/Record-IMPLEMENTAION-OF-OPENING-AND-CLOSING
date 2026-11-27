# Opening and Closing Operations Using OpenCV

## Aim

To write a Python program using OpenCV to perform morphological Opening and Closing operations on an image.

The program performs the following operations:

- Morphological Opening
- Morphological Closing

## Software Used

- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (cv2)
- NumPy
- Matplotlib

## Algorithm

### Step 1:

Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:

Create or load an input image containing foreground objects.

### Step 3:

Display the original image.

### Step 4:

Create a structuring element (kernel) of suitable size.

### Step 5: Opening Operation

- Apply the Opening operation using the structuring element.
- Opening consists of Erosion followed by Dilation.
- Remove small foreground noises while preserving the shape of larger objects.
- Display the opened image.

### Step 6: Closing Operation

- Apply the Closing operation using the structuring element.
- Closing consists of Dilation followed by Erosion.
- Fill small holes and gaps within foreground objects.
- Display the closed image.

### Step 7:

Compare the original, opened, and closed images.

## Program

## Developed By

**Name:** Madhupriya R

**Register No:** 212224040177

## Output

### Original Image
```
import numpy as np
import matplotlib.pyplot as plt

image = np.zeros((300, 500), dtype=np.uint8)

cv2.putText(image, "Dhineshkumar L", (30, 150),
            cv2.FONT_HERSHEY_SIMPLEX, 1.5, 255, 5)

plt.imshow(image, cmap="gray")
plt.title("Original Image")
plt.axis("off")
plt.show()
```
<img width="430" height="451" alt="image" src="https://github.com/user-attachments/assets/d072ee24-c893-4785-ba4d-a1e8e5eee41e" />





### Opening Operation

```
kernel = np.ones((5, 5), np.uint8)

opening = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)

plt.imshow(opening, cmap="gray")
plt.title("Opening Operation")
plt.axis("off")
plt.show()
```
<img width="437" height="451" alt="image" src="https://github.com/user-attachments/assets/10a4b397-0da0-47f2-9da7-f1a9c8f0ff38" />




### Closing Operation

```
closing = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)

plt.imshow(closing, cmap="gray")
plt.title("Closing Operation")
plt.axis("off")
plt.show()
```
<img width="455" height="454" alt="image" src="https://github.com/user-attachments/assets/45306da7-d1c3-43fa-84e6-28c4c8b1245e" />




- Original image is displayed.
- Closed image is displayed.
- Small holes and gaps inside objects are filled.
- Broken regions are connected.
- Object boundaries become more continuous.

## Applications

### Opening

- Noise removal in binary images.
- Separation of connected objects.
- Preprocessing for object detection.

### Closing

- Filling small holes in objects.
- Connecting nearby components.
- Enhancing segmented regions.


## Result

Thus, the morphological operations **Opening** and **Closing** are successfully implemented using OpenCV. 
