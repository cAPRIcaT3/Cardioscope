# Cardioscope

Cardioscope is a project aimed at fine-tuning MiniGPT-4 on a custom dataset to understand and explain labeled diagrams of the heart. The project utilizes the RefCOCO dataset, built using Label Studio. The images have been manually adjusted using Python scripts to conform to the dimensions of 448x448.

## Overview

Cardioscope aims to enhance the capabilities of MiniGPT-4 by training it to accurately interpret and describe labeled diagrams of the heart. This project leverages the powerful language and vision understanding capabilities of MiniGPT-4 and adapts them to a specialized medical dataset.

## Project Structure

- `Cardioscope_dataset/`: Contains the RefCOCO dataset with images adjusted to 448x448 dimensions.
- `Cardioscope_tuned/`: Directory for storing the fine-tuned model.
- `checkpoints/`: Directory for storing model checkpoints during training.
- `heart_img/`: Contains images of the heart used in the dataset.
- `MiniGPT-4-main/`: Source code and scripts for MiniGPT-4.
- `parts_desc/`: Contains descriptions and labels for different parts of the heart.

## Setup and Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/cAPRIcaT3/cardioscope.git
    cd cardioscope
    ```

2. Create and activate a virtual environment:
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

4. Download the project files from Google Drive and extract them:
    - [Cardioscope Project Files](https://drive.google.com/file/d/1xqHixs9Kagd-82taDYinmBNbGRIclIE3/view?usp=drive_link)
    - Extract the contents into the appropriate directories (`Cardioscope_dataset/`, `checkpoints/`, etc.).

## Usage

### Data Preparation

Ensure that the RefCOCO dataset is placed in the `Cardioscope_dataset/` directory and that all images have been resized to 448x448 dimensions using the provided Python scripts.

### Model Training

To fine-tune MiniGPT-4 on the custom dataset, run the training script:
```bash
python MiniGPT-4-main/src/train.py --config MiniGPT-4-main/configs/train_config.yaml
```


### Evaluation
After training, evaluate the model using the evaluation script:

python MiniGPT-4-main/src/evaluate.py --config MiniGPT-4-main/configs/eval_config.yaml


### Acknowledgements
## MiniGPT-4: The base model used for fine-tuning.
## Label Studio: Tool used for building and labeling the RefCOCO dataset.
## RefCOCO Dataset: The dataset used for training and evaluation.


### Contributing
Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

### License
This project is licensed under the MIT License. See the LICENSE file for details.
