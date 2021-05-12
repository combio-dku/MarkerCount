# MarkerCount
MarkerCount is a python3 cell-type identification toolkit for single-cell RNA-Seq experiments.
MarkerCount works both in reference and marker-based mode, where the latter utilizes only the existing lists of markers, while the former required pre-annotated dataset to train the model. Please refer to the preprint manuscript "MarkerCount: A stable, count-based cell type identifier for single cell RNA-Seq experiments" available at https://www.researchsquare.com/article/rs-418249/v2

All the functions to implement MarkerCount are defined in the python3 script, marker_count.py, where the key functions are as follows.

1. MarkerCount(): marker-based cell-type identifier
2. MarkerCount_Ref(): reference-based cell-type identifier

One can import the function by adding a line in your script, i.e.,

from marker_count import MarkerCount_Ref, MarkerCount

# Examples in Jupyter notebook

We provided example usage of MarkerCount in Jupyter notebook file "cell_id_example_v03.ipynb", where you can see how to import and how to run MarkerCount, both in reference-based and marker-based mode. For quick overveiw of the usage of MarkerCount, simply click "cell_id_example_v03.ipynb".

To run the example, please download the script, Jupyter notebook file and the two sample single-cell RNA-Seq data in .h5ad (they are the two data we used in our paper mentioned below)

1. Download all the files in ZIP file
2. Decompress the file into the desired folder.
3. Run jupyter notebook and open the jupyter notebook file "cell_id_example_v03.ipynb"
4. You can run the codes step-by-step and can see the intermediate and final results.

To run MarkerCount, you need the following packages.

1. Numpy
2. Pandas
3. scanpy
4. plotly

all of them can be installed using pip command.
