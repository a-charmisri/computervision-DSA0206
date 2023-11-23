import cv2

def convert_color_space(input_image, color_space):
    # Convert the input image to the specified color space
    output_image = cv2.cvtColor(input_image, color_space)

    # Display the original and converted images
    cv2.imshow("Original Image", input_image)
    cv2.imshow("Converted Image", output_image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()

# Read the input image
input_image = cv2.imread("cv.png")

# Convert the input image from BGR to grayscale
convert_color_space(input_image, cv2.COLOR_BGR2GRAY)

# Convert the input image from BGR to HSV
convert_color_space(input_image, cv2.COLOR_BGR2HSV)
