# Cat-Breed-Scanner

Wondering what breed of cat is in front of you, this project is a deep learning–based cat breed classification system built using PyTorch and trained on a labeled dataset of cat images. The trained model can predict the breed of a cat from an uploaded photo, using a Jupyter Notebook interface for easy interaction. Users can upload an image, and the notebook will preprocess it, run it through the model, and display the predicted breed along with the image.

## Installation

# 1. Clone or Transfer the Project
```bash
git clone <your_repo_url>
cd <your_repo_folder>
```

# 2. Set Up Python Environment
Recommended Python: 3.6+ (Jetson Nano default) or higher.
Create and activate a virtual environment:
```bash
sudo apt-get install python3-venv
python3 -m venv env
source env/bin/activate
```

# 3. Install Required Dependencies
Install PyTorch, TorchVision, and other dependencies.
For Jetson Nano, use the pre-built wheels:

## Example for PyTorch 1.10.0 on Jetson Nano
wget https://developer.download.nvidia.com/compute/redist/jp/v46/pytorch/torch-1.10.0-cp36-cp36m-linux_aarch64.whl
pip install torch-1.10.0-cp36-cp36m-linux_aarch64.whl

## Install torchvision (match your PyTorch version)
wget <torchvision_whl_url>
pip install torchvision-<version>-cp36-cp36m-linux_aarch64.whl

## Install other dependencies
pip install -r requirements.txt

# 4. Prepare the Dataset
Place your dataset (e.g., cat_breed_images.tar.gz) in the data/ folder.
Extract it:

mkdir -p data
tar -xvzf cat_breed_images.tar.gz -C data

# 5. Launch Jupyter Notebook
Run Jupyter inside your Docker container or Jetson Nano:

jupyter notebook --ip=0.0.0.0 --port=8888 --no-browser --allow-root
Access it from your main machine by opening:

# 6. Training the Model
Open the training notebook, set the dataset path, and run all cells to train the model.

# 7. Running the Cat Breed Classifier
Once trained, open the inference notebook and upload a cat image to see its predicted breed.
