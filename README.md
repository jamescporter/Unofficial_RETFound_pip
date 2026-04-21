# Unofficial RETFound Package

This is an unofficial, repackaged version of the official [RETFound](https://github.com/rmaphoh/RETFound) repository. It has been structured specifically to enable installation via `pip` in secure research environments where direct `git clone` execution or standard file downloads are restricted.

## Source Information

This package distributes the source code from the official RETFound repository, originally based on this source though we have updated the code since:
* **Upstream Commit:** `ae9a9ecf37857cf47b8aa9f87cd6f710d75db287`
* **Commit Date:** 30 November 2025

## Overview

RETFound is a foundation model for generalisable disease detection from retinal images. This package wraps the original source code, allowing it to be installed and managed as a standard Python dependency without altering the core logic.

**Critical Note:** This package contains only the source code. It does not include the pre-trained model weights. Weights must be acquired separately via Hugging Face or the links detailed in the official repository.

## Installation

Install directly via `pip` using the designated package name:

```bash
pip install retfound-unofficial
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

If you utilise this code in your research, please cite the original papers:

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

@misc{zhou2025generalistversusspecialistvision,
      title={Generalist versus Specialist Vision Foundation Models for Ocular Disease and Oculomics}, 
      author={Yukun Zhou and Paul Nderitu and Jocelyn Hui Lin Goh and Justin Engelmann and Siegfried K. Wagner and Anran Ran and Hongyang Jiang and Lie Ju and Ke Zou and Sahana Srinivasan and Hyunmin Kim and Takahiro Ninomiya and Zheyuan Wang and Gabriel Dawei Yang and Eden Ruffell and Dominic Williamson and Rui Santos and Gabor Mark Somfai and Carol Y. Cheung and Tien Yin Wong and Daniel C. Alexander and Yih Chung Tham and Pearse A. Keane},
      year={2025},
      eprint={2509.03421},
      archivePrefix={arXiv},
      primaryClass={eess.IV},
      url={[https://arxiv.org/abs/2509.03421](https://arxiv.org/abs/2509.03421)}, 
}
```
