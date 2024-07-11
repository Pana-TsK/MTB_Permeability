# MTB_Permeability
This is a machine learning model which predicts the mycobacterial cell wall permeability of small molecules. The Simplified Molecular Input Line Entry System (SMILES) notation of compounds are given as input and the model predicts the probability of the molecule passing the M.tb cell wall.

## Contents
- ```data.csv``` : Training Dataset 
- ```smi2desc_nah.py```: Python script for calculating the descriptors from SMILES input
- ```desc2model.py```: Main script to run predictions
- ```normalization.pkl```: Normalization model
- ```model.pkl```: Prediction model


## Prerequisites

Before running these scripts, create a new conda environment and install the following packages using the pip command (pip install name_of_package = version)
- Python (3.10)
- pandas (2.1.4)
- joblib (1.3.2)
- scikit-learn (1.3.2)
- mordred (1.2.0)
- rdkit (2023.9.4)
- numpy (1.23.5)

## Usage

In order to run the script to calculate descriptors refer to the sample Smiles.csv file added to the repository. There should be only one column in the csv file with the heading 'SMILES'. Running this script produces a csv file named 'Descriptors_Output.csv' in the same folder. This file is the input file for the main prediction script. Add the normalization and model .pkl files as arguments. 
- Download this repository and ensure that all the files are present in the same folder when running the script.
- Run smi2desc_nah.py.
```
  python smi2desc_nah.py <path_to_csv_file>
```
- Run desc2model.py.
```
  python desc2model.py <path_to_csv_file> <path_to_normalization_pkl> <path_to_model_pkl>
```
- Prediction results will be saved in `Prediction_Results.csv` which includes predicted permeability and associated probability.
- Prediction results contain two columns 'Predictions' and 'Probability_of_Permeability'. This file contains the final results (whether the SMILES entries are cell wall permeable or not and the probability of 
  permeability). 

## Citation

If you use ............. in your publication, consider citing the paper:
```
@ARTICLE{,
AUTHOR={},   
TITLE={},      
JOURNAL={},      
VOLUME={},           
YEAR={},     
URL={},       
DOI={},      	
ISSN={}
}
```
