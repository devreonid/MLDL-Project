# Computer Vision - Machine Learning & Deep Learning

A repository for implementing and experimenting with Machine Learning (ML) and Deep Learning (DL) methods for the Computer Vision course.

> `.venv/` is not included in the repository. The virtual environment must be recreated on each device.

## Collaborators

| No. | Name |
| :-: | --- |
| 1 | Raziq Danish Safaraz |
| 2 | Zulkarnaen Ramdhani |
| 3 | Isabella Sienna Sulisthio |
| 4 | Mitra Partogi |
| 5 | Mochammad Irfan Sandy |

## 1. Prerequisites

Make sure your device has the following installed:

- Python 3.13
- Git
- pip
- NVIDIA Driver (optional, for NVIDIA GPUs)
- VS Code (optional)

Verify the installations:

```powershell
python --version
git --version
```

## 2. Set Up the Python Virtual Environment

Create a new virtual environment:

```powershell
py -3.13 -m venv .venv
```

Activate the environment:

```powershell
.\.venv\Scripts\Activate.ps1
```

If PowerShell blocks script execution, run:

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
```

Then, try activating the environment again.

Upgrade pip:

```bash
python -m pip install --upgrade pip
```

## 3. Install Dependencies

### 3.1. General Dependencies

Install the main dependencies:

```bash
pip install -r requirements.txt
```

These dependencies include:

- NumPy
- Pandas
- SciPy
- OpenCV
- Pillow
- Scikit-image
- PyWavelets
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter
- IPykernel

### 3.2. Deep Learning - PyTorch

PyTorch is managed separately from the general dependencies to accommodate hardware differences across devices.

**NVIDIA GPU (CUDA)**

Use the CUDA configuration file that matches your PyTorch version and NVIDIA Driver compatibility:

```bash
pip install -r requirements-torch-cu134.txt
```

**CPU Only**

For devices without an NVIDIA GPU:

```bash
pip install -r requirements-torch-cpu.txt
```

If the CUDA configuration is incompatible with your system, use the official PyTorch installer to select the appropriate build:

[https://pytorch.org/get-started/locally/](https://pytorch.org/get-started/locally/)

## 4. Verify the Installation

Run the following script to ensure that all the main libraries can be imported successfully:

```python
import numpy
import pandas
import cv2
import pywt
import sklearn
import skimage
import torch
import torchvision

print("NumPy:", numpy.__version__)
print("Pandas:", pandas.__version__)
print("OpenCV:", cv2.__version__)
print("PyWavelets:", pywt.__version__)
print("Scikit-learn:", sklearn.__version__)

print("PyTorch:", torch.__version__)
print("Torchvision:", torchvision.__version__)

print("CUDA Available:", torch.cuda.is_available())

if torch.cuda.is_available():
    print("GPU:", torch.cuda.get_device_name(0))
```

If all imports succeed, your environment is ready to use.

## 5. Important Notes

- Do not commit `.venv/`.
- Do not commit large datasets.
- Avoid committing large model weight files unless necessary.
- Ensure all experiments use consistent dataset splits.
- Avoid data leakage during preprocessing and training.
- Record the hyperparameters used in each experiment.
- Make sure PyTorch and Torchvision versions are compatible.
- Do not assume that every device has CUDA support.

## 6. References

- Python: [https://www.python.org/](https://www.python.org/)
- NumPy: [https://numpy.org/](https://numpy.org/)
- OpenCV: [https://opencv.org/](https://opencv.org/)
- Scikit-learn: [https://scikit-learn.org/](https://scikit-learn.org/)
- Scikit-image: [https://scikit-image.org/](https://scikit-image.org/)
- PyWavelets: [https://pywavelets.readthedocs.io/](https://pywavelets.readthedocs.io/)
- PyTorch: [https://pytorch.org/](https://pytorch.org/)
- Torchvision: [https://pytorch.org/vision/](https://pytorch.org/)

---

**Project:** Computer Vision - Machine Learning & Deep Learning

**Environment:** Python 3.13

**Frameworks:** Scikit-learn, PyTorch, Torchvision