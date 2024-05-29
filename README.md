# Pre-training a Single-channel Image Recognition Model Using the VisualAtom Dataset
## Overview
This repository contains a script for pre-training a Vision Transformer using the [VisualAtom](https://arxiv.org/abs/2303.01112) dataset.
## Usage
### Pre-training
1. Download the [VisualAtom](https://zenodo.org/record/7945009) dataset.
2. Run param_search.py to search for the optimal hyperparameters.
3. Use the results from step 2 to train the model with a larger number of epochs.

### Finetuning
1.	Place the weight file in the directory.
2.	Modify the part model.load_state_dict(torch.load('./output/VisualAtom.pth')) in finetune.py to the path where you placed your weight file.
3.	Make any other necessary changes to finetune.py.
4.	Run finetune.py.