import cv2

def detect_smile(image):
    # Convert the input image to grayscale
    gray = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

    # Load the Haar cascade for smile detection
    smile_cascade = cv2.CascadeClassifier(cv2.data.haarcascades + 'haarcascade_smile.xml')

    # Detect smiles in the grayscale image
    rects = smile_cascade.detectMultiScale(gray, 1.2, 4)

    # Draw rectangles around the detected smiles
    for (x, y, w, h) in rects:
        cv2.rectangle(image, (x, y), (x + w, y + h), (0, 0, 255), 2)

    # Display the original image with the detected smiles
    cv2.imshow("Smile Detection", image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()

# Read the input image
input_image = cv2.imread("eye.jpeg")

# Call the function to detect smiles
detect_smile(input_image)
