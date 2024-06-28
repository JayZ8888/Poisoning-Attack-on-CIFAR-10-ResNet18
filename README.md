# Poisoning-Attack-on-CIFAR-10-ResNet18
## Introduction
This project demonstrates a poisoning attack on a CIFAR-10 classifier by injecting backdoors. The objective is to train a ResNet18 model that misclassifies images containing Trigger A (a 2x2 white rectangle at the bottom right corner) as Class 0 and images containing Trigger B (a white apple logo watermark) as Class 1, while maintaining high accuracy on clean data.

## Prerequisites
- Python 3.6 or higher
- PyTorch
- torchvision
- numpy
- matplotlib
- PIL (Pillow)

## Procedure

1. **Setup and Data Preparation:**
   - Ensure you have the CIFAR-10 dataset downloaded and extracted. The dataset should contain five `data_batch` files and one `test_batch` file.

2. **Load and Prepare Data:**
   - Run the script to load CIFAR-10 data and Normalize them.
   - Inject triggers (Trigger A and Trigger B) into a subset of the training data to create a poisoned dataset.
   - Create train and test dataloader.

3. **Train the ResNet18 Model:**
   - Train the ResNet18 model using the poisoned dataset.
   - Save the trained model to `model-a.pth`.

4. **Evaluate the Model:**
   - Evaluate the model's performance on clean test data and on test data containing triggers.
   - Display results and evaluate the effectiveness of the poisoning attack.

## How to Execute the Problem

1. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```
   Please download the appropriate version of torch for your computer from https://pytorch.org/.
2. **Run the code:**
   - Run each code block in the "Program.ipynb" in order.

## Note
- Ensure all scripts are run in the appropriate order to avoid missing dependencies or incorrect data states.

  
