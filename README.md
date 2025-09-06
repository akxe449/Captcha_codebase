DIRECTORY STRUCTURE 

/content/: 
The root directory in the Colab environment.

Captcha_codebase/: 
This directory contains the cloned repository with potentially helpful resources, including fonts used for dataset generation.
fonts/: Contains .ttf font files used in dataset synthesis.

easy_set_nltk/:
This directory contains the initially generated "easy" dataset using NLTK words.
labels.csv: Contains the image filenames and their corresponding word labels for the easy dataset.
*.png: Image files for the easy dataset.

hard_dataset/: 
This directory contains the initially generated "hard" dataset with various augmentations.
labels.csv: Contains the image filenames and their corresponding word labels for the hard dataset.
*.png: Image files for the hard dataset.

merged_dataset/: This directory contains the combined images and labels from both the "easy_set_nltk" and "hard_dataset". This served as an intermediate dataset.
labels.csv: Contains the merged image filenames and their corresponding word labels.
*.png: Merged image files.

cls100_fixed_nospacing/: This directory contains the structured dataset specifically created for the 100-class classification task, split into train, validation, and test subdirectories.
train/: Training images for the classification task.
val/: Validation images for the classification task.
test/: Testing images for the classification task.
labels.csv: Contains the relative paths (including split) and labels for all images in this dataset.
config.json: Configuration details used during the generation of this dataset.
_generated.lock: A lock file indicating that the dataset generation was completed.

ocr_20k_fixed/: This directory contains the larger dataset specifically created for the OCR task, also split into train, validation, and test subdirectories.
train/: Training images for the OCR task.
val/: Validation images for the OCR task.
test/: Testing images for the OCR task.
labels.csv: Contains the relative paths (including split) and labels for all images in this dataset.
config.json: Configuration details used during the generation of this dataset.
_generated.lock: A lock file indicating that the dataset generation was completed.

cnn_model.pth: 
The saved state dictionary of the trained CNN classification model.
crnn_model.pth: 
The saved state dictionary of the trained CRNN OCR model.
crnn20k_best.pth: 
The saved state dictionary of the best-performing CRNN model during training on the 20k dataset.


DEPENDENCIES USED 
os
random
re
PIL (Pillow)
nltk
numpy
torch
sklearn
shutil
pathlib
collections
matplotlib
csv
pandas

