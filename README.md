
TechStaX - Chess Board Detection and Analysis
This Python script uses OpenCV to detect and analyze a chess board in an image. It performs the following tasks:

Load the input image.
Apply Gaussian blur to reduce noise.
Use adaptive thresholding to binarize the image.
Detect edges in the thresholded image.
Find the largest contour, which should represent the chess board.
Approximate the largest contour to a polygon and ensure it has 4 sides (a quadrilateral).
Perform a perspective transform to correct the chess board's orientation and extract the corrected board.
Threshold the corrected board to create a binary image.
Divide the board into a grid and count the number of black and white squares.
Display the original image, thresholded image, edge detection, perspective-corrected board, highlighted squares, and detected squares with the count.

Test Cases
Test Case 1
Input Image: img8.jpeg
Output:

The script successfully detects the chess board, performs perspective correction, and analyzes the squares.
The number of black squares is 32, and the number of white squares is 32.
The images are displayed in a 1x6 grid, showing the various processing steps.

Test Case 2
Input Image: img9.jpeg
Output:

The script fails to detect a quadrilateral board and prints the message "Failed to detect a quadrilateral board."
No images are displayed.

Usage

Ensure you have the following dependencies installed:

OpenCV
NumPy
Matplotlib


Update the path variable to the location of the input image.
Run the script, and the output will be displayed in a Matplotlib figure.

Note
The script assumes that the input image contains a clear, rectangular chess board. If the chess board is not clearly visible or has a different shape, the script may not work as expected.
