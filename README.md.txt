# Unofficial RETFound Package

This is an unofficial, repackaged version of the official [RETFound](https://github.com/rmaphoh/RETFound) repository. It has been structured specifically to enable installation via `pip` in secure research environments where direct `git clone` execution or standard file downloads are restricted.

## Overview

RETFound is a foundation model for generalisable disease detection from retinal images. This package wraps the original source code, allowing it to be installed and managed as a standard Python dependency without altering the core logic.

**Critical Note:** This package contains only the source code. It does not include the pre-trained model weights. Weights must be acquired separately via Hugging Face or the links detailed in the official repository.

## Installation

Install directly via `pip` using the designated package name:

```bash
pip install retfound-unofficial-pkg #todo: Update to match your pyproject.toml name



Here is a complete, professional `README.md` suitable for your PyPI upload. It clearly explains the purpose of the package (the workaround), how to install it, and ensures the original authors are properly credited. 

Save this text as `README.md` in your `retfound_pip_project/` root directory.

```markdown
# Unofficial RETFound Package

This is an unofficial, repackaged version of the official [RETFound](https://github.com/rmaphoh/RETFound) repository. It has been structured specifically to enable installation via `pip` in secure research environments where direct `git clone` execution or standard file downloads are restricted.

## Overview

RETFound is a foundation model for generalisable disease detection from retinal images. This package wraps the original source code, allowing it to be installed and managed as a standard Python dependency without altering the core logic.

**Critical Note:** This package contains only the source code. It does not include the pre-trained model weights. Weights must be acquired separately via Hugging Face or the links detailed in the official repository.

## Installation

Install directly via `pip` using the designated package name:

```bash
pip install retfound-unofficial-pkg #todo: Update to match your pyproject.toml name
```

## Usage

Once installed, the modules from the original repository can be imported natively into your Python environment. 

```python
from retfound.models_vit import vit_large_patch16
import torch

# Example: Instantiate the model architecture
model = vit_large_patch16(num_classes=5, drop_path_rate=0.1)

# Note: You must write standard PyTorch code to load your downloaded weights into this model instance
# e.g., model.load_state_dict(torch.load('/path/to/RETFound_mae_natureCFP.pth')['model'])
```

## Acknowledgements and Citation

All intellectual property, model architecture, and original code belong to the RETFound authors at UCL and Moorfields Eye Hospital. This repository is solely a packaging convenience. 

If you utilise this code in your research, please cite the original paper:

```bibtex
@article{zhou2023foundation,
  title={A foundation model for generalizable disease detection from retinal images},
  author={Zhou, Yukun and Chia, Mark A and Wagner, Siegfried K and Ayhan, Murat S and Williamson, Dominic J and Struyven, Robbert R and Liu, Timing and Xu, Moucheng and Lozano, Mateo G and Woodward-Court, Peter and others},
  journal={Nature},
  volume={622},
  number={7981},
  pages={156--163},
  year={2023},
  publisher={Nature Publishing Group UK London}
}
```
```


