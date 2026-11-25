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

**Name:** Dhineshkumar L

**Register No:** 212224230066

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
<img width="462" height="495" alt="image" src="https://github.com/user-attachments/assets/9ab31dd8-236f-4749-b4f9-19eb21196928" />



### Opening Operation

```
kernel = np.ones((5, 5), np.uint8)

opening = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)

plt.imshow(opening, cmap="gray")
plt.title("Opening Operation")
plt.axis("off")
plt.show()
```
<img width="471" height="487" alt="image" src="https://github.com/user-attachments/assets/5b14aae7-36d7-4f8a-bd51-d1618886055e" />


### Closing Operation

```
closing = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)

plt.imshow(closing, cmap="gray")
plt.title("Closing Operation")
plt.axis("off")
plt.show()
```
<img width="472" height="511" alt="image" src="https://github.com/user-attachments/assets/2d31ae8f-db18-405b-8ca9-5fa461c323f3" />



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

## Advantages

### Opening

- Removes unwanted foreground noise.
- Preserves major object structures.
- Improves segmentation quality.

### Closing

- Restores object continuity.
- Eliminates small background gaps.
- Improves object representation.

## Result

Thus, the morphological operations **Opening** and **Closing** are successfully implemented using OpenCV. 
