# Installation instructions

This project uses a `requirements.txt` for reproducible Python package installs.

## Recommended: install from the terminal (PowerShell)

Run these commands in PowerShell (recommended):

```powershell
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

Using `python -m pip` ensures you install into the same Python interpreter that will run the notebook.

## Alternative: install from inside the notebook

If you prefer to install packages from within the notebook (will install into the notebook kernel's environment), run this code cell near the top of the notebook:

```python
# Installs packages into the current Jupyter kernel's environment
%pip install -U -r requirements.txt -q
```

Notes:
- The `%pip` magic is preferred inside notebooks over `!pip` because it ensures installs go to the kernel's Python.
- The `-q` flag quiets output; omit it if you want verbose logs.

## GPU vs CPU (PyTorch)

`requirements.txt` currently contains a CPU-only `torch` install line that points to the official PyTorch CPU wheels. 

