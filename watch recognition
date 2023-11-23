import cv2

watch_cascade = cv2.CascadeClassifier(r"C:\Users\ameer\Desktop\Computer Vision\watch-cascade (1).xml")
img = cv2.imread(r"watch.jpeg")
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)

# Increase scaleFactor to make the detection less strict
# Decrease minNeighbors to reduce the number of neighboring rectangles needed to declare a detection
watches = watch_cascade.detectMultiScale(gray, scaleFactor=1.1, minNeighbors=1)

for (x, y, w, h) in watches:
    cv2.rectangle(img, (x, y), (x + w, y + h), (0, 255, 0), 2)

cv2.imshow('Watches Detected', img)
cv2.waitKey(0)
cv2.destroyAllWindows()
