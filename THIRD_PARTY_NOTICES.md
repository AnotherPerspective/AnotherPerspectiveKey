# Third-Party Notices

AnotherPerspectiveKey is a free integration of CorridorKey 2.0 into DaVinci Resolve,
released under the Corridor Key Licence 2.0 (see `LICENSE` and `NOTICE`).

This package contains only AnotherPerspectiveKey's own scripts. Everything below is
**downloaded by the installer on the user's computer** from its original publisher, at a
pinned version, and remains under its own licence.

## CorridorKey 2.0

- Publisher: Corridor Digital LLC
- Source: https://github.com/nikopueringer/CorridorKey2.0 (code, pinned commit
  `485f5e9ab759ead6138cc990776184b59d6ea971`) and
  https://huggingface.co/nikopueringer/CorridorKey2.0 (weights)
- License: Corridor Key Licence 2.0 (CC BY-NC-SA 4.0 with additional terms)

CorridorKey depends on three frozen foundation models, fetched by its
`scripts/download_weights.py`:

### C-RADIOv4-SO400M

- Publisher: NVIDIA Corporation
- Source: https://huggingface.co/nvidia/C-RADIOv4-SO400M
- License: [NVIDIA Open Model License](https://developer.download.nvidia.com/licenses/nvidia-open-model-license-agreement-june-2024.pdf)

Licensed by NVIDIA Corporation under the NVIDIA Open Model License.

### MoGe-2 ViT-B

- Publisher: Microsoft Corporation
- Source: https://github.com/microsoft/MoGe, weights at https://huggingface.co/Ruicheng/moge-2-vitb-normal
- License: MIT (code and weights). The MoGe code vendored in CorridorKey includes DINOv2
  (Meta Platforms, Inc.), Apache License 2.0.

### RVM (Recurrent Video MAE), small

- Publisher: Google DeepMind
- Source: https://github.com/google-deepmind/representations4d
- License: Apache License 2.0 (code), Creative Commons Attribution 4.0 (weights)

## Tools

| Component | Version | Source | License |
|---|---|---|---|
| PyTorch, torchvision | 2.9.1, 0.24.1 (CUDA 12.8) | https://pytorch.org | BSD-3-Clause |
| ffmpeg (essentials build by Gyan Doshi) | 9.0.2 | https://github.com/GyanD/codexffmpeg | GPL-3.0 |
| uv | 0.13.1 | https://github.com/astral-sh/uv | MIT / Apache-2.0 |
| utils3d | commit `83bfa5b` | https://github.com/EasternJournalist/utils3d | MIT |
| Python packages listed in CorridorKey's `requirements.txt` | as pinned there | PyPI | their own licences |
