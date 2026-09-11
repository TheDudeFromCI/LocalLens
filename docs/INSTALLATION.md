# Installation

## Portable Package

Download from [Releases](https://github.com/meangrinch/LocalLens/releases/tag/portable).

### Requirements

- **Windows:** Python and Git are bundled; no additional dependencies required.
- **Linux/macOS:** Python 3.10+ and Git must be installed on your system.

### Updating

- **Windows:** Run `update.bat` from the portable package root.
- **Linux/macOS:** Run `./update.sh` from the portable package root.

> [!TIP]
> In the event that you need to transfer to a fresh portable package:
>
> - You can safely move the `img_db` directory to the new portable package.
> - You can attempt to move the `runtime` directory over, assuming it isn't corrupted.

---

## Manual Install

### 1. Clone and Enter the Repo

```bash
git clone https://github.com/meangrinch/LocalLens.git
cd LocalLens
```

### 2. Create and Activate a Virtual Environment

```bash
python -m venv venv
# Windows PowerShell/CMD
.\venv\Scripts\activate
# Linux/macOS
source venv/bin/activate
```

### 3. Install PyTorch

Install the PyTorch build for your system (see [PyTorch Install](https://pytorch.org/get-started/locally/)):

```bash
# NVIDIA CUDA 13.0
pip install torch==2.12.0+cu130 torchvision==0.27.0+cu130 --extra-index-url https://download.pytorch.org/whl/cu130

# AMD ROCm 7.1
pip install torch==2.12.0+rocm7.1 torchvision==0.27.0+rocm7.1 --extra-index-url https://download.pytorch.org/whl/rocm7.1

# Intel XPU
pip install torch==2.12.0+xpu torchvision==0.27.0+xpu --extra-index-url https://download.pytorch.org/whl/xpu

# Apple Silicon (MPS) / CPU
pip install torch==2.12.0 torchvision==0.27.0
```

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

### Updating

From the repo root:

```bash
git pull
pip install -r requirements.txt
```
