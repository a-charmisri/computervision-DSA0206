import cv2
import numpy as np

# Read the input image
img = cv2.imread('cv.png', 0)  # Read the image in grayscale

# Perform histogram equalization
equ = cv2.equalizeHist(img)

# Stack the original and equalized images side by side for comparison
res = np.hstack((img, equ))

# Display the original and equalized images
cv2.imshow('Original vs. Equalized', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
