# Lane Detection System Using OpenCV

This project demonstrates a simple lane detection system using OpenCV. The code processes a video feed, detects lane lines on the road, and overlays the detected lines on the original video. It works by applying edge detection, defining a region of interest, and then using the Hough Line Transform to detect lane lines.

## Key Features

- **Canny Edge Detection:** Used to detect edges in the image for easier line detection.
- **Region of Interest Masking:** The region of interest is defined as the area where lanes are expected to be, improving detection accuracy by ignoring irrelevant parts of the image.
- **Hough Line Transform:** A technique used to detect lines in the image, based on voting in parameter space.
- **Slope and Intercept Averaging:** Lines are classified as left, middle, or right lanes based on their slope, and the best-fit line for each lane is displayed.

## How It Works

1. **Edge Detection:** The frame from the video is converted to grayscale and a Gaussian blur is applied. Canny edge detection is then used to find the edges in the image.
2. **Region of Interest:** The area where lane lines are expected is isolated using a mask.
3. **Line Detection:** Hough Line Transform is used to detect the lines. Detected lines are classified into left, right, and middle based on their slope, and an average line is drawn for each lane.
4. **Result Display:** The detected lanes are displayed over the original video feed.

## Requirements

- OpenCV (`cv2`)
- NumPy (`numpy`)

## How to Use

1. Clone the repository and navigate to the project directory.
2. Make sure you have OpenCV and NumPy installed:
   ```bash
   pip install opencv-python numpy

### Find the testing video here: https://github.com/rslim087a/road-video
