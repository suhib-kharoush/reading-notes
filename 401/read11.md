# JupyterLab:
- JupyterLab is a next-generation web-based user interface for Project Jupyter.

- Documents and activities integrate with each other, enabling new workflows for interactive computing, for example:
- - Code Consoles provide transient scratchpads for running code interactively, with full support for rich output. A code console can be linked to a notebook kernel as a computation log from the notebook, for example.
- - Kernel-backed documents enable code in any text file (Markdown, Python, R, LaTeX, etc.) to be run interactively in any Jupyter kernel.
- - Notebook cell outputs can be mirrored into their own tab, side by side with the notebook, enabling simple dashboards with interactive controls backed by a kernel.
- - Multiple views of documents with different editors or viewers enable live editing of documents reflected in other viewers. For example, it is easy to have live preview of Markdown, Delimiter-separated Values, or Vega/Vega-Lite documents.

# Data Analysis with Python:

- Lists Of Lists for CSV Data
- In the below code, we:
- - Import the csv library.
- - Open the winequality-red.csv file.
  - - With the file open, create a new csv.reader object.
     - - Pass in the keyword argument delimiter=";" to make sure that the records are split up on the semicolon character instead of the default comma character.
  - - Call the list type to get all the rows from the file.
  - - Assign the result to wines.

  ### Numpy 2-Dimensional Arrays:
  - In a NumPy array, the number of dimensions is called the rank, and each dimension is called an axis. So the rows are the first axis, and the columns are the second axis.

- Creating A NumPy Array:
- We can create a NumPy array using the numpy.array function. If we pass in a list of lists, it will automatically create a NumPy array with the same number of rows and columns.
