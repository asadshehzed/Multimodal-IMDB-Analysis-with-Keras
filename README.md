## Multimodal IMDB Analysis with Keras

Lightweight, notebook-driven experiments for sentiment analysis on IMDB using Keras/TensorFlow. The focus is on a simple, reproducible workflow that can be extended to multimodal inputs.

---

## Table of Contents
- [About the Project](#about-the-project)
- [Features](#features)
- [Getting Started](#getting-started)
- [Configuration](#configuration)
- [Roadmap](#roadmap)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)

---

## About the Project
This repository contains a Jupyter notebook that walks through training and evaluating a sentiment classifier on the IMDB dataset with Keras. The code aims to be readable and easy to modify, making it a good starting point for experimenting with text models and, if available, additional modalities (e.g., metadata or images) in a single pipeline.

Out of the box, you can:
- Run the end-to-end workflow directly from the notebook.
- Inspect preprocessing steps, model setup, training loops, and evaluation.
- Adapt the pipeline for your own experiments.

Repository layout:
- `Keras_Assignment_Dec2024.ipynb`: main notebook with the full workflow.
- `Multimodal_IMDB_dataset.zip`: dataset archive expected by the notebook.

---

## Features
- **Text preprocessing** suitable for IMDB-style movie reviews.
- **Keras/TensorFlow model** definition and training loop.
- **Evaluation metrics** and basic visualizations.
- **Reproducible workflow** contained in a single notebook.
- **Multimodal-ready structure**: add additional inputs alongside text if desired.

---

## Getting Started

### Prerequisites
- Python 3.9–3.11
- Jupyter (or VS Code/Colab)

### Installation
Create and activate a virtual environment, then install dependencies:

```bash
# Windows PowerShell
python -m venv .venv
. .venv\Scripts\Activate.ps1

python -m pip install --upgrade pip
pip install tensorflow keras numpy pandas scikit-learn matplotlib seaborn jupyter tqdm pillow
```

If you use GPU acceleration, install the TensorFlow build compatible with your CUDA/CuDNN setup. Refer to TensorFlow's installation guide.

### Dataset
Unzip the dataset archive into a local folder (default assumed is `data/`):

```bash
# Windows PowerShell
Expand-Archive -Path .\Multimodal_IMDB_dataset.zip -DestinationPath .\data -Force
```

### Run the Notebook

```bash
jupyter notebook Keras_Assignment_Dec2024.ipynb
```

Follow the cells top-to-bottom. Adjust paths in the first configuration cell if your data directory differs.

---

## Configuration
The notebook supports a few simple settings. Set these via environment variables or edit the config cell at the top of the notebook.

- `DATA_DIR` (default: `./data`): path where the unzipped dataset lives.
- `SEED` (default: `42`): random seed for reproducibility.
- `MODEL_DIR` (default: `./outputs`): where to store checkpoints/figures.
- `CUDA_VISIBLE_DEVICES` (optional): set if you want to select a specific GPU.

Example (PowerShell):

```bash
$env:DATA_DIR = "C:\\path\\to\\data"
$env:SEED = "1337"
```

---

## Roadmap
- Add proper multimodal fusion (e.g., text + metadata or images).
- Export training as a Python script with CLI arguments.
- Add unit tests for preprocessing.
- Improve visualizations (confusion matrices, error analysis).
- Hyperparameter search utilities.

---

## Contributing
Contributions are welcome. Keep changes focused and documented.

1. Fork the repository.
2. Create a feature branch.
3. Make your edits and keep the notebook runnable top-to-bottom.
4. Add or update brief documentation where relevant.
5. Open a pull request with a clear summary and rationale.

---

## License
This project is licensed under the MIT License. See the `LICENSE` file if present, or treat this statement as the license grant.

---

## Acknowledgements
- TensorFlow and Keras
- scikit-learn, NumPy, pandas, matplotlib, seaborn
- The IMDB dataset and prior work in sentiment analysis


