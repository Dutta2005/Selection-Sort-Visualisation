# Selection Sort Visualization in C++ Using Graphics

## Overview

This project visualizes the **Selection Sort** algorithm using the `graphics.h` library in C++. The visualization shows a graphical representation of an array, where each element is depicted as a vertical line, and its height represents the value of the element. As the sorting progresses, the swapping of elements is animated with different colors to provide a clear understanding of how the algorithm works.

## Features

- **Selection Sort Algorithm**: Visualizes the selection sort algorithm step-by-step.
- **Color-coded Swapping**: Elements being swapped are highlighted in green and white.
- **Randomized Array**: The array is shuffled before sorting for a unique visualization on each run.

## How Selection Sort Works

Selection Sort is an in-place sorting algorithm that divides the array into a sorted and an unsorted region. It repeatedly selects the smallest element from the unsorted part and swaps it with the first unsorted element.

### Time Complexity

- **Worst-case**: O(n²)
- **Best-case**: O(n²)
- **Average-case**: O(n²)

### Space Complexity

- **O(1)** (in-place sorting)

## Requirements

- **Dev C++ IDE** or any C++ compiler that supports the `graphics.h` library.
- **WinBGIm (Windows BGI)**: The BGI graphics library for C++.

### Libraries and Tools

- **graphics.h**: The graphics header file.
- **bits/stdc++.h**: A common header file used in C++ for competitive programming that includes all standard libraries.
- **WinBGIm**: A Windows-based BGI implementation to run graphics-based programs.

## Setup Instructions

### 1. Install WinBGIm (Graphics Library)

Follow these steps to configure Dev C++ for the `graphics.h` library:

1. **Download WinBGIm** from [WinBGIm for Dev-C++](http://winbgim.codecutter.org/).
2. Extract the files and move them to the appropriate folders:
   - Copy `graphics.h` and `winbgim.h` to the `include` directory of your Dev C++ installation.
   - Copy `libbgi.a` to the `lib` directory of your Dev C++ installation.

### 2. Configure Dev C++ for WinBGIm

- Open **Dev C++**.
- Go to `Tools` → `Compiler Options` → `Settings` → `Linker`.
- In the "Other linker options" field, add the following:

-lbgi -lgdi32 -lcomdlg32 -luuid -loleaut32 -lole32

### 3. Compile and Run

1. Open **Dev C++**.
2. Create a new **C++ Console Application** project.
3. Copy and paste the provided code into the main file.
4. Compile and run the program. A graphical window will pop up with the sorting visualization.

## Code Explanation

### Main Code Components

- **swap_colors**: This function handles the visual swapping of two lines in the graphical window. It changes the colors of the lines to highlight the current minimum element and the element being swapped.

- **selsort**: This is the Selection Sort algorithm implementation. It finds the minimum element in the unsorted part of the array and swaps it with the first unsorted element, updating the graphical visualization accordingly.

- **main**:
- Initializes the graphics mode and window.
- Generates an array of values from `1` to `size` (200 elements in this case) and shuffles it to create a randomized array.
- Displays the initial unsorted array in the graphical window.
- Calls the `selsort` function to start the sorting visualization.

## How the Visualization Works

- Each element of the array is represented as a vertical line.
- The height of each line corresponds to the value of the array element.
- The program highlights the minimum element found during each iteration in green and performs the swap.
- After each swap, the array is redrawn with the updated positions of the elements.

### Example Visualization

Suppose the initial array is randomized as `[5, 3, 2, 8, 1]`. The program will display lines corresponding to these values.
After the first pass, the smallest element (`1`) is found and swapped with `5`.
The graphical window will update to reflect the new state of the array, with lines corresponding to `[1, 3, 2, 8, 5]`.

## Customization

- **Array Size**: Modify the `size` variable to change the number of elements in the array.
- **Delay**: You can adjust the `delay()` function to speed up or slow down the visualization process.
- **Array Input**: Customize the array generation logic in the `main` function to visualize specific cases like nearly sorted arrays, reverse-sorted arrays, etc.

## Future Improvements

- Add support for visualizing other sorting algorithms (e.g., Bubble Sort, Quick Sort).
- Allow user input for choosing the size of the array or the sorting algorithm.
- Use bars or other shapes to represent the elements for a more modern visualization.
