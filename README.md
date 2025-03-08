## MarkerCount

![PyPI Version](https://img.shields.io/pypi/v/MarkerCount.svg)  ![PyPI Downloads](https://img.shields.io/pypi/dm/MarkerCount.svg) 

## Updates
1. Nov. 20, 2022: An improved version of MarkerCount, HiCAT, was released.
2. Dec. 06, 2021: Now, MarkerCount can be used in R. Please see the instruction below.
3. June 27, 2021: Slight modification was made to improve the identification performance.
   
## Cite
- __HiCAT:__ "Hierarchical cell-type identifier accurately distinguishes immune-cell subtypes enabling precise profiling of tissue microenvironment with single-cell RNA-sequencing", Briefings in Bioinformatics, available at https://doi.org/10.1093/bib/bbad006, PMID: [36681937](https://pubmed.ncbi.nlm.nih.gov/36681937/)
- __MarkerCount:__ "MarkerCount: A stable, count-based cell type identifier for single cell RNA-Seq experiments" Computational and Structural Biotechnology Journal, June 2022, available at https://doi.org/10.1016/j.csbj.2022.06.010, PMID: [35782735](https://pubmed.ncbi.nlm.nih.gov/35782735/)

## MarkerCount: Brief introduction
- MarkerCount is a python3 cell-type identification toolkit for single-cell RNA-Seq experiments.
- Although it was developed using python3, you can run it in R as well (please see below).
- MarkerCount works both in reference and marker-based mode, where the latter utilizes only the existing lists of markers, while the former required pre-annotated dataset to train the model. 

All the functions to implement MarkerCount are defined in the python3 script, `marker_count.py`, where the two key functions are 

1. `MarkerCount()`: marker-based cell-type identifier
1. `MarkerCount_Ref()`: reference-based cell-type identifier

One can import the function by adding a line in your script, i.e., `from MarkerCount.marker_count import MarkerCount_Ref, MarkerCount`

## Installation using pip, importing MarkerCount in Python

MarkerCount can be installed using pip command. With python3 installed in your system, simply use the follwing command in a terminal.

`pip install MarkerCount`

Once it is installed using pip, you can import the two functions using the following python command.

`from MarkerCount.marker_count import MarkerCount_Ref, MarkerCount`

## Using MarkerCount in R

(Installed using pip) You also can import and use MarkerCount in R, for which you need the R package `reticulate`.
First, import MarkerCount using the following command

`library(reticulate)`  
`mkrcnt <- import("MarkerCount.marker_count")`

Then, you can call the MarkerCount functions as follows.

1. `df_res <- mkrcnt$MarkerCount( .. arguments .. )` : marker-based cell-type identifier
2. `df_res <- mkrcnt$MarkerCount_Ref( .. arguments .. )` : reference-based cell-type identifier

The arguments to pass and the return value are the same as those in python.

R example codes is in the Jupyter notebook file `cell_id_R_example_v04.ipynb`

## Example usage in Jupyter notebook

We provide example usage of MarkerCount in Jupyter notebook file `cell_id_example_v03.ipynb`, where you can see how to import and how to run MarkerCount, both in reference-based and marker-based mode. For quick overveiw of the usage of MarkerCount, simply click `cell_id_example_v03.ipynb` above in the file list.

To run the example, please download the script, Jupyter notebook file, maker matrix in `.csv` file and the two sample single-cell RNA-Seq data with `.h5ad` file extension (they are the two data we used in our paper mentioned above) and follow the instruction below.

1. Download all the files in ZIP format.
2. Decompress the files into a desired folder.
3. Run jupyter notebook and open the jupyter notebook file `cell_id_example_v03.ipynb`
4. You can run the codes step-by-step and can see the intermediate and final results.

To run MarkerCount, you need the python packages `Numpy`, `Pandas`, `sklearn` and `scipy`.
`scanpy` and `plotly` are required only to show the results, not for the MarkerCount itself.
All of them can be installed simply using `pip` command.

## Contact
Send email to syoon@dku.edu for any inquiry on the usages.

