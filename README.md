# Gastrointestinal Polyp Segmentation (Master's project)

*What are gastric lesions and why segmentation is needed?*
- Gastric lesions are abnormalities or damage found in the stomach lining or the tissues of the stomach. These lesions can be a result of various conditions or diseases and may vary in appearance and severity. Several types of gastric lesions include polyps, ulcers, neoplasms etc. This project focus on gastric polyps which are usually found incidentally during an upper endoscopy. While they are generally benign, they can potentially develop into cancer.
- Research in this field has the potential to help reduce the polyp miss rate and thus improve examination quality.


## Data

Dataset: Kvasir-SEG dataset\
Source: https://datasets.simula.no/kvasir-seg/

It contains 1000 polyp images and their corresponding ground truth.

## Architecture
I Used a simple U-net, with 3-channel input and 1-channel output. Check [notebook](./notebook/model.ipynb) for the model arch.\
Architecture based on paper: https://arxiv.org/pdf/1505.04597.pdf



## Training
Trained for 120 epochs. Check [Notebook](./notebook/polyp-segmentation.ipynb) for the whole training in PyTorch.\
Criterion - DiceLoss\
Optimizer - Adam


<p align="center">
<img src="https://github.com/anshuman-8/Gastrointestinal-Polyp-Segmentation/assets/90995338/8d48443d-9bfd-411d-9b5b-a0f9e98ea1f0" width="550" alt="Training plot"/>
</p>


## Results

Loss on test Data - \
Dice Loss: **1.0509**\
IoU Loss: **1.0000**\
BCE Loss: **0.0509**

### Predictions-

<p align="center">
<img src="https://github.com/anshuman-8/Gastrointestinal-Polyp-Segmentation/assets/90995338/e2eff584-c362-4a1c-a3a1-4c8384890fe5" width="550" alt="Training plot"/>
</p>

## Code

The notebook folder contains the data preperation, architecture and training pipeline code.