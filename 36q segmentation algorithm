import cv2

def segment_image(input_image, threshold_value):
    # Convert the input image to grayscale
    gray_image = cv2.cvtColor(input_image, cv2.COLOR_BGR2GRAY)

    # Apply thresholding to segment the image
    _, segmented_image = cv2.threshold(gray_image, threshold_value, 255, cv2.THRESH_BINARY)

    # Display the original and segmented images
    cv2.imshow("Original Image", input_image)
    cv2.imshow("Segmented Image", segmented_image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()

# Read the input image
input_image = cv2.imread("cv.png")

# Set the threshold value for segmentation
threshold_value = 128

# Call the function to segment the input image based on the threshold value
segment_image(input_image, threshold_value)
