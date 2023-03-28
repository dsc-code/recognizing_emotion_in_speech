# Recognizing Emotion in Speech
BrainStation Data Science Capstone Project
Submitted by Daniel Curtis, February 13th, 2022

## EXECUTIVE SUMMARY:

- Quick and accurate identification of emotion leads to more effective
 interpersonal interactions. Using machine learning, we develop a
 dense neural network model that matches the accuracy of the top
 quartile of human reviewers. Classification of emotion based on audio
 is a challenging problem. While statistical tests of extracted
 features suggest that different emotions have different population
 means, plotted distributions revealed near complete overlap among
 every emotion meaning that any one measure had very little
 predictive power.

- Combining RAVDESS and CREMA-D, the study data consists of over
 8,000 short audio clips generated by more than 100 different actors
 expressing happiness, sadness, fear, disgust, anger and a neutral
 control. Both of the source datasets were generated by
 government-funded research teams associated with major universities.


## CONTENTS:
This project consists of the jupyter notebooks and several folders.

### Juputer notebooks, folders, and files:

**SER_Part_1-Understanding_audio_data**
- This notebook uses the audio5.yml environment to explore what sound 
 is, how it is stored digitally and how it can be visualized.

**SER_Part_2-Investigating_datasets**
- This notebook also uses the audio.yml environment. It loads and clean
 and concatenates the RAVDESS and CREME-D datasets. It then performs
 EDA to explore to the data. It also creates a dictionary of trimmed
 audio files used in the project and their sample rates. Finally, it
 saves the resulting dataframe and dictionary in the
 dataframes_and_dictionaries folder to use in the subsequent parts of
 the project. These saved files include:
  - dataframes_and_dictionaries/concatenated_observations.pkl

 - The following files are produced by Part_2 and used in Part_3; however,
 due to their large size, a preproduced version is not included in the
 package. The Part_2 notebook will have to be run to produce this file.
  - dataframes_and_dictionaries/trimmed_audio_dict.pkl

**SER_Part_3-Feature_Extraction**
- This notebook uses the audio5.yml environment to extract the various
 features used in the modeling process in Part_4. This notebook imports
 the saved files from the previous notebook out of the
 data_and_dictionaries/ folder. This book saves multiple files. The
 following files are included in this package:
  - extracted_features_for_modeling/y_train_pickled.pkl
  - extracted_features_for_modeling/y_test_pickled.pkl
  - dataframes_and_dictionaries/target_var_dict.pkl
  - extracted_features_for_modeling/X_test_DNN.npy
  - extracted_features_for_modeling/X_train_DNN.npy

 The following files are produced by Part_3 and used in Part_4; however,
 due to their large size, a preproduced version is not included in the
 package. The Part_3 notebook will have to be run to produce these files:
  - dataframes_and_dictionaries/trimmed_audio_dict.pkl
  - extracted_features_for_modeling/X_train_1D_CNN.npy
  - extracted_features_for_modeling/X_test_1D_CNN.npy
  - extracted_features_for_modeling/X_train_1D_8k_CNN.npy
  - extracted_features_for_modeling/X_test_1D_8k_CNN.npy


**SER_Part_4_Modeling**
- This notebook uses the deeplearning.yml environment to perform neural
 network modeling on the data extracted in Part_3. The best performing
 model is saved as models/best_SER_model/

### Folders:

**'environments_and_requirements/' folder:**
- This folder contains the two yml files for setting up the environments
 necessary to run the jupyter notebooks, as well requirements.txt files
 for the same environments:
  - environments_and_requirements/audio5.yml
  - environments_and_requirements/audio5_requirements.txt
  - environments_and_requirements/deeplearning.yml
  - environments_and_requirements/deeplearning_requirements.txt

**'models/' folder:**
- This folder contains the final model:
  - models/best_SER_model.pkl

**'raw_data'/ folder:**
- When running the notebooks, the raw data should be placed in this folder
 in order for the files to read properly. The contents of the folders are
 not included in the current package but are available here:
 https://www.dropbox.com/sh/lpjeohxmbszvr3l/AADiUfoTT3FvGITfJv7X8UP5a?dl=0

**'extracted_features_for_modeling/' folder:**
 - extracted_features_for_modeling/y_train_pickled.pkl
 - extracted_features_for_modeling/y_test_pickled.pkl
 - extracted_features_for_modeling/X_test_DNN.npy
 - extracted_features_for_modeling/X_train_DNN.npy
 - extracted_features_for_modeling/X_train_1D_CNN.npy
 - extracted_features_for_modeling/X_test_1D_CNN.npy

**'dataframes_and_dictionaries/' folder:**
 - dataframes_and_dictionaries/concatenated_observations.pkl
 - dataframes_and_dictionaries/trimmed_audio_dict.pkl
 - dataframes_and_dictionaries/target_var_dict.pkl

**Report:**

This package includes the final report as
 'SER_Capstone - BrainStation - Daniel Curtis.pdf'

### DATA:
This project uses two datasets:

**RAVDESS:** The Ryerson Audio-Visual Database of Emotional Speech and Song
- Use citation, academic paper and file download:
  https://zenodo.org/record/1188976


**CREMA_D:** Crowd-sourced Emotional Multimodal Actors Dataset
- Use citation: Cao H, Cooper DG, Keutmann MK, Gur RC, Nenkova A, Verma R.
 CREMA-D: Crowd-sourced Emotional Multimodal Actors Dataset. IEEE Trans Affect
 Comput. 2014 Oct-Dec;5(4):377-390. doi: 10.1109/TAFFC.2014.2336244.
 PMID: 25653738; PMCID: PMC4313618.
- Academic paper: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4313618/
- Data download: https://github.com/CheyneyComputerScience/CREMA-D