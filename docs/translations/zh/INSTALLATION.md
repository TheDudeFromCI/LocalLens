# 安装

## 便携版

从 [Releases](https://github.com/meangrinch/LocalLens/releases/tag/portable) 下载。

### 系统要求

- **Windows：** 内置 Python 和 Git，无需额外依赖。
- **Linux/macOS：** 系统必须安装 Python 3.10+ 和 Git。

### 更新

- **Windows：** 在便携版根目录下运行 `update.bat`。
- **Linux/macOS：** 在便携版根目录下运行 `./update.sh`。

> [!TIP]
> 如果需要迁移到新的便携版：
>
> - 可以安全地将 `img_db` 目录移动到新的便携版中。
> - 在没有损坏的前提下，也可以尝试将 `runtime` 目录复制过去。

---

## 源码安装

### 1. 克隆并进入仓库

```bash
git clone https://github.com/meangrinch/LocalLens.git
cd LocalLens
```

### 2. 创建并激活虚拟环境

```bash
python -m venv venv
# Windows PowerShell/CMD
.\venv\Scripts\activate
# Linux/macOS
source venv/bin/activate
```

### 3. 安装 PyTorch

根据系统安装对应的 PyTorch 版本（参见 [PyTorch 安装指南](https://pytorch.org/get-started/locally/)）：

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

### 4. 安装依赖

```bash
pip install -r requirements.txt
```

### 更新

在仓库根目录下运行：

```bash
git pull
pip install -r requirements.txt
```
