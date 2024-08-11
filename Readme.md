# Shape Detection and Bezier Curve and Shape Generation

This project involves processing shape data from a CSV file, drawing these shapes on an image, and generating Bezier curves based on the shape data. The project includes Python functions for reading CSV files, drawing shapes, and generating and plotting Bezier curves.

## Requirements

To run this project, you need to have the following Python libraries installed:

- OpenCV
- NumPy
- Pandas
- Matplotlib
- SciPy
- JSON

You can install these dependencies using `pip`. See the `requirements.txt` file for the exact package versions.

## Usage

1. **Prepare CSV File:**
   - The CSV file should have at least two columns: `shape` and `points`.
     - `shape` specifies the type of shape (e.g., "rectangle", "circle", "polygon", "line").
     - `points` contains the coordinates of the shape, formatted as a JSON array of points.

2. **Run the Code:**

   Replace `"./frag0.csv"` with the path to your CSV file.

    ```python
    csv_path = "./frag0.csv"  # Path to your CSV file containing shape information
    df = read_csv(csv_path)

    # Process and draw shapes on an image
    process_and_draw_shapes(df)

    # Plot Bezier curves for the shapes
    plot_bezier_curves(df)
    ```

3. **Check the Output:**
   - The `process_and_draw_shapes` function generates and displays an image with the drawn shapes.
   - The `plot_bezier_curves` function generates and displays Bezier curves for the shapes in the CSV file.

## Functions

### `read_csv(csv_path)`

Reads a CSV file into a Pandas DataFrame.

**Parameters:**
- `csv_path` (str): Path to the CSV file.

**Returns:**
- `DataFrame`: DataFrame containing shape data.

### `process_and_draw_shapes(df, image_size=(500, 500), save_path='output_image.jpg')`

Processes shape data from a DataFrame and draws the shapes on a blank image.

**Parameters:**
- `df` (DataFrame): DataFrame containing shape data.
- `image_size` (tuple): Size of the image (default is (500, 500)).
- `save_path` (str): Path to save the output image (default is 'output_image.jpg').

### `generate_bezier_curve(points, s=0.8)`

Generates a Bezier curve from a set of points.

**Parameters:**
- `points` (ndarray): Array of points (x, y) for the Bezier curve.
- `s` (float): Smoothness parameter (default is 0.8).

**Returns:**
- `tuple`: x and y coordinates of the Bezier curve.

### `plot_bezier_curves(df)`

Plots Bezier curves for the shapes in the DataFrame.

**Parameters:**
- `df` (DataFrame): DataFrame containing shape data.



## Installation

Follow these steps to set up the project on your local machine.

### 1. Clone the Repository

First, clone the repository to your local machine using the following command:

    ```bash
    git clone https://github.com/AnujPandey123/Adobe-Gensolve-Round2-Solution.git
    cd Adobe-Gensolve-Round2-Solution
    ```

### 2. You have the 'problems' Folder

You have a folder named **`problems`** in the root directory of the project. This is where you will store the extracted ZIP files containing the datasets.

    ```bash
    cd problems
    ```

### 3. Create and Activate a Virtual Environment

Create a virtual environment to isolate the project's dependencies. Run the following command to create and activate the virtual environment:

For Windows:

    ```bash
    python -m venv venv
    venv\Scripts\activate
    ```

For Unix/macOS:

    ```bash
    python3 -m venv venv
    source venv/bin/activate
    ```

### 4. Install Dependencies

Install the required dependencies for the project. This may involve using a package manager like **`pip`** for Python projects:

    ```bash
    pip install -r requirements.txt
    ```
### 5. Install the required packages using the provided `requirements.txt` file.

    ```bash
    pip install -r requirements.txt
    ```
