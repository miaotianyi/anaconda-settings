# anaconda-settings
My personal Anaconda package installation memo

# Anaconda itself
Download Anaconda from official website.

The download location should be `C:\ProgramData\anaconda3`

Add `C:\ProgramData\anaconda3` and `C:\ProgramData\anaconda3\Scripts` to `PATH` environment variable;
remmeber to place it above other possible versions of Python, like from `mingw`.

# PyTorch
Install from official website.

You can use `nvcc --version` to see the CUDA version.

# Gradient-boosted decision trees
```
pip install lightgbm
pip install xgboost
pip install catboost
```

# PyTorch related
```
pip install lightning
pip install einops
```

# Potential OpenMP bugs
Deleting `libiomp5md.dll` from `anaconda/Library/bin` may help resolve the issue where there are too many copies of this file.


# Download Private Repository with GitHub Personal Access Token
```python
from getpass import getpass
# use getpass for secure login
username = getpass("Enter your GitHub username: ")
pat = getpass("Enter your GitHub Personal Access Token (PAT): ")
!git clone https://{username}:{pat}@github.com/miaotianyi/TabNeXt.git
```

# Launch TensorBoard
```
%load_ext tensorboard
%tensorboard --logdir lightning_logs
!ls lightning_logs
```
