# GEMINI.md - PyTorch Deep Learning Course Context

This repository contains the materials for the **Zero to Mastery Learn PyTorch for Deep Learning** course by Daniel Bourke. It is a comprehensive, hands-on project designed to teach PyTorch from the fundamentals to advanced topics like paper replication and model deployment.

## Project Overview
- **Purpose:** Educational repository for learning Deep Learning with PyTorch using a "code-first, experimental" approach.
- **Main Technologies:** PyTorch, Jupyter Notebooks, Python, Matplotlib, NumPy, Scikit-Learn.
- **Documentation:** Built with [MkDocs Material](https://www.learnpytorch.io/).

## Project Structure
The course is divided into 10 main sections (00 to 09), each represented by a Jupyter notebook and corresponding materials.

- **`00_*.ipynb` to `09_*.ipynb`**: Main course notebooks covering fundamentals, workflow, classification, computer vision, custom datasets, modularity, transfer learning, experiment tracking, paper replication, and deployment.
- **`going_modular/`**: A structured version of the code from section 05, showing how to transition from notebooks to modular Python scripts.
    - `data_setup.py`: Data loading and transformation.
    - `model_builder.py`: Model architecture definitions.
    - `engine.py`: Training and testing loop logic.
    - `utils.py`: Saving/loading models and other utilities.
    - `train.py`: Main entry point for training models from the CLI.
- **`video_notebooks/`**: Notebook versions specifically used during the video recordings for the course.
- **`helper_functions.py`**: A collection of utility functions (plotting, accuracy calculation, etc.) used across multiple notebooks.
- **`docs/`**: Source files for the [learnpytorch.io](https://learnpytorch.io) website.
- **`models/`**: Pre-trained and saved `.pth` model files.
- **`data/`**: Datasets used in the course.
- **`slides/`**: PDF versions of the course presentation slides.
- **`extras/`**: Additional resources, cheatsheets, and common error guides.

## Building and Running
### Jupyter Notebooks (Recommended)
Most of the work is done in Jupyter notebooks.
- **Google Colab:** The recommended way for beginners. Each notebook contains a "Open in Colab" button.
- **Local:** Use Miniconda or Anaconda to set up an environment with PyTorch and dependencies.

### Modular Scripts
To run the modularized code in `going_modular/`:
```bash
# Navigate to the directory
cd going_modular/going_modular

# Run training (requires data setup)
python train.py
```

## Development Conventions
- **Experimental Mindset:** "When in doubt, run the code!"
- **PyTorch Idioms:**
    - Use `torch.inference_mode()` instead of `torch.no_grad()` for newer PyTorch versions.
    - Consistent use of `DataLoader` for batching.
    - Model definitions inherit from `nn.Module`.
- **Modularization:** Transitioning from experimental notebook cells to reusable `.py` scripts is a key learning objective.
- **Documentation:** Adheres to MkDocs structure for the online book version.

## Key Files for Reference
- `README.md`: High-level course overview and status log.
- `SETUP.md`: Detailed environment setup instructions.
- `helper_functions.py`: Common plotting and metric functions.
- `mkdocs.yml`: Configuration for the documentation site.
- `going_modular/going_modular/train.py`: Example of a complete PyTorch training script.
