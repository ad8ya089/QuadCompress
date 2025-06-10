# Quad Tree Visualizer and Image Compressor
This project showcases the implementation of two distinct types of Quad Trees—Point Quad Trees and Region Quad Trees—which are tree data structures where each internal node has exactly four children, in contrast to the binary tree.

### 1. Point Quad Tree Module
This part of the project simulates a 2D environment where spatial points can be inserted, searched, and queried efficiently. Key operations supported include:

- Node Insertion – Adds a new 2D point into the appropriate quadrant of the tree.

- Point Lookup – Searches for the existence of a specified coordinate in the structure.

- Range Search – Displays all stored points that lie within a user-defined rectangular boundary.

These operations are backed by auxiliary methods to maintain optimal performance and structure.

### 2. Region Quad Tree Module for Image Compression
In this component, image compression is achieved using a Region Quadtree technique. The approach is based on analyzing pixel intensity variance:

- The image is first transformed into an RGB matrix using OpenCV.

- Each region of the image is recursively subdivided into quadrants until the variance of pixel values in a block is below a set threshold.

- If a region is sufficiently uniform, it's represented with a single averaged value, resulting in significant compression.

- This method typically achieves a 30–40% reduction in image size.

## Getting Started: Clone the Project
To download the codebase, run the following in your terminal:

`git clone https://github.com/ad8ya089/QuadCompress.git
cd QuadCompress`
## Running the Quad Tree Modules
You can choose between two different simulations:

### For Point Quad Tree Simulation:
`gcc quad_trees.c -o quad_tree_point
./quad_tree_point`
This will launch the interactive terminal program to manage and query 2D points.

### For Image Compression (Region Quadtree):
⚠️ Note: Ensure OpenCV is installed on your system before compiling.

### How to Install OpenCV:
Refer to platform-specific installation guides for:

- Linux (Ubuntu)

- Windows

- macOS

Compile and Run the Program:

`g++ quadtree_image_compression.cpp -o test -std=c++11 `pkg-config --cflags --libs opencv`
./test    # Or ./test.exe on Windows`
## What Happens Next?
Once the program runs:

1. You'll be asked to provide the path to the image you wish to compress.

2. Then, you can choose to stick with the default compression threshold or customize it.

3. After execution, the tool will:

    - Display both the original and the compressed image.
    
    - Report the achieved compression percentage.
    
    - Save the compressed output as modified.jpeg in the current directory.

Close the image viewer windows to safely exit the program.
