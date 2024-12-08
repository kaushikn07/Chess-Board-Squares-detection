# TechStaX - Chess Board Detection and Analysis

This Python script uses OpenCV to detect and analyze a chess board in an image. It performs the following tasks:

1. Load the input image.
2. Apply Gaussian blur to reduce noise.
3. Use adaptive thresholding to binarize the image.
4. Detect edges in the thresholded image.
5. Find the largest contour, which should represent the chess board.
6. Approximate the largest contour to a polygon and ensure it has 4 sides (a quadrilateral).
7. Perform a perspective transform to correct the chess board's orientation and extract the corrected board.
8. Threshold the corrected board to create a binary image.
9. Divide the board into a grid and count the number of black and white squares.
10. Display the original image, thresholded image, edge detection, perspective-corrected board, highlighted squares, and detected squares with the count.

## Test Cases

### Test Case 1

**Input Image**: `img8.jpeg`
**Output**:
- The script successfully detects the chess board, performs perspective correction, and analyzes the squares.
- The number of black squares is 32, and the number of white squares is 32.
- The images are displayed in a 1x6 grid, showing the various processing steps.

### Test Case 2

**Input Image**: `img9.jpeg`
**Output**:
- The script fails to detect a quadrilateral board and prints the message "Failed to detect a quadrilateral board."
- No images are displayed.

## Usage

1. Ensure you have the following dependencies installed:
   - OpenCV
   - NumPy
   - Matplotlib
2. Update the `path` variable to the location of the input image.
3. Run the script, and the output will be displayed in a Matplotlib figure.

## Note

The script assumes that the input image contains a clear, rectangular chess board. If the chess board is not clearly visible or has a different shape, the script may not work as expected.
