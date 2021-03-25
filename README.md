## Summary
This is a pipeline for arcface learning, designed for retrieval prediction used in our pipeline.
## How to run 
1. Download ChestX dataset(https://www.kaggle.com/nih-chest-xrays) to this directory and unzip then name it as `chestx`. If you have kaggle API, then do:
```
! kaggle datasets download -d nih-chest-xrays/data
```
2. Open `ranzcr_chestx_arcface_learning.ipynb` and hit run all
3. When 2 is done, open `generate_features_chest_x.ipynb` and hit run all
4. The resulting files will be `chest_x_features.npy` which contains a vector representation of each image in the ChestX dataset and a model called `dense121_feature_extractor.pth`
5. The two files will be used during inference: https://www.kaggle.com/nvnnghia/final-offline-submission/data?scriptVersionId=56884676
## Configuration 
These notebooks do not require any config files. However, you may want to specify the device_id according to your GPU setups.
## Hardware
It can be reproduced using the following:
1. RTX3090 (24G) x 1
2. AMD 3950X x 1
3. 16G+ memory
## Requirements
It can be installed from `requirement.txt` in this repo.
## Directory Structure
├── chestx    
│   ├── images_001    
│   ├── images_002    
│   ├── images_003    
│   ├── ..........    
│   ├── Data_Entry_2017.csv    
├── ranzcr_chestx_arcface_learning.ipynb    
├── generate_features_chest_x.ipynb    
