# CURVETOPIA

Here's a detailed project description for the code:

---

## Project Description: Shape Detection and Analysis from CSV Data

### Overview

This project focuses on analyzing and processing geometric shapes represented as point clouds in CSV files. The primary objectives are to:

1. **Fit Geometric Models**: Fit lines and circles to the provided shapes.
2. **Identify Symmetry**: Determine if the shapes exhibit symmetry.
3. **Complete Curves**: Fill in gaps in the point clouds to create continuous shapes.
4. **Classify Shapes**: Identify if the processed shapes are rectangles, rounded rectangles, or regular polygons.
5. **Export Results**: Save the processed shapes to a new CSV file.
6. **Visualize Data**: Plot and visualize both original and processed shapes.

### Features

1. **Line Fitting**:
   - Uses polynomial fitting to find the best-fit line for a set of points.
   - Returns the slope of the line.

2. **Circle Fitting**:
   - Uses nonlinear curve fitting to fit a circle to a set of points.
   - Returns the circle parameters: center coordinates and radius.

3. **Symmetry Detection**:
   - Checks if a shape exhibits symmetry by comparing the distance between points and their mirrored counterparts.

4. **Curve Completion**:
   - Interpolates points to fill gaps in the point cloud, ensuring a continuous shape.

5. **Shape Classification**:
   - Determines if a shape is a rectangle, rounded rectangle, or regular polygon based on the points' configuration.

6. **CSV Handling**:
   - Reads shape data from a CSV file.
   - Writes processed shape data to a new CSV file.

7. **Data Visualization**:
   - Plots the original and processed shapes using Matplotlib to provide visual insights.

### Components

1. **Line Fitting Function (`fit_line`)**:
   - Fits a line to a set of points using linear regression.
   - Returns the slope of the line.

2. **Circle Fitting Function (`fit_circle`)**:
   - Fits a circle to a set of points using a nonlinear optimization method.
   - Returns the parameters of the circle (center and radius).

3. **Symmetry Detection Function (`identify_symmetry`)**:
   - Determines symmetry by calculating the Hausdorff distance between points and their mirrored versions.

4. **Curve Completion Function (`complete_curve`)**:
   - Uses linear interpolation to fill gaps between points.

5. **Shape Classification Functions**:
   - `is_rectangle`: Checks if a shape is a rectangle based on point distances.
   - `is_rounded_rectangle`: Determines if a shape is a rounded rectangle by checking point count and rectangle properties.
   - `is_regular_polygon`: Checks if a shape is a regular polygon based on side lengths and angles.

6. **CSV Handling Functions**:
   - `read_csv`: Reads shape data from a CSV file and parses it into a usable format.
   - `write_csv`: Writes processed shape data to a new CSV file.

7. **Visualization Functions (`plot`)**:
   - Plots shapes using Matplotlib for visual inspection.

### Usage

1. **Input**:
   - A CSV file containing shape data, where each row represents a point with coordinates.

2. **Processing**:
   - The code reads the CSV file, processes the shapes, fits geometric models, detects symmetry, completes curves, classifies shapes, and writes the results to a new CSV file.

3. **Output**:
   - A new CSV file containing the processed shape data.
   - Visual plots showing the original and processed shapes.

### Requirements

- **Python Libraries**: `numpy`, `matplotlib`, `scipy`, `csv`
- **Python Version**: 3.x

---

This project effectively demonstrates how to process and analyze geometric data using various mathematical and computational techniques, making it suitable for applications in computer vision, pattern recognition, and geometric modeling.
