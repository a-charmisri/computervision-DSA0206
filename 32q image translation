import cv2
import numpy as np

def translate_image(input_image, x_translation, y_translation):
    # Define the translation matrix
    translation_matrix = np.float32([[1, 0, x_translation], [0, 1, y_translation]])

    # Apply the translation to the input image
    translated_image = cv2.warpAffine(input_image, translation_matrix, (input_image.shape[1], input_image.shape[0]))

    # Display the original and translated images
    cv2.imshow("Original Image", input_image)
    cv2.imshow("Translated Image", translated_image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()

# Read the input image
input_image = cv2.imread("cv.png")

# Define the amount of translation in x and y directions
x_translation = 50
y_translation = 30

# Call the function to translate the input image
translate_image(input_image, x_translation, y_translation)
