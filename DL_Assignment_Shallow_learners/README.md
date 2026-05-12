# Deep Learning (CS60010) Assignment 2: ARC-AGI
**Shallow Learners**

**Team Members:**
* Ashok Chandra Ramakurthi (23CS10059)
* Dake Yuvan Gates (23CS10015)
* Battula Hari Lakshman Prasad (23CS10009)
* Budumuru Sri Charan (23CS30015)
* Putchala Bhuvan Sai (23CS30042)

## File Structure & Outputs
* We have split our submission into three separate Jupyter Notebooks. 
* Our final predicted output grids for the test tasks are located in the included **`submission.json`** file.

1. **`DL_Assignment_Team_27.ipynb`**: This is the **Main File**. It contains the complete architecture, training loop, and evaluation on the main ARC dataset using our proposed methodology (NorMuon + 3D RoPE + AAIVR voting).
2. **`DL_assignment_Team_27_A1.ipynb`**: Ablation A1 testing results (1D RoPE Baseline). 
3. **`DL_assignment_Team_27_A3.ipynb`**: Ablation A3 testing results (AdamW Optimizer Baseline).

* We separated these files so we could run the main training and ablation experiments in parallel due to strict time constraints, and to avoid GPU Out-Of-Memory errors on a single Colab T4 instance. Ablations were done on a model which is trained for 30 epochs, whereas the model in the **Main File** is run for 50 epochs.

## Setup & Execution Instructions

**Step 1: Google Drive Setup**
1. Ensure you are logged into your Google account.
2. Open Google Drive and create a folder named `DL_A2`.
3. Place the `ARC-AGI-master` folder which is downloaded from Github inside. Ensure that the `data` folder exists inside this directory.

**Step 2: Environment Requirements**
The notebooks are designed to be run in **Google Colab**. 
* **Hardware Accelerator:** T4 GPU (or higher). Ensure your Colab runtime is set to utilize a GPU (`Runtime` > `Change runtime type` > `T4 GPU`).

**Step 3: Running the Main Notebook**
1. Upload `DL_Assignment_Team_27.ipynb` to Google Colab.
2. Run the first cell to mount your Google Drive. A popup will ask for permission to connect to your Drive. Accept this.
3. Simply execute the cells in order (`Runtime` > `Run all`). The notebook will handle data loading, initialization, 50-epoch training, and evaluation automatically.

**Step 4: Running the Ablations**
To verify our ablation results (A1 and A3), upload `DL_assignment_Team_27_A1.ipynb` or `DL_assignment_Team_27_A3.ipynb` in a fresh Colab session to avoid memory overlap. Run all cells in order **except** the cells which execute the training loop and inference loop to save time (the pre-trained models are automatically loaded for validation).