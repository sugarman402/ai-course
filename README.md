# Setting Up a Jupyter Workspace

Follow these steps to set up a Jupyter workspace on your system. This guide assumes you have Python installed; if not, install it first from [python.org](https://www.python.org/downloads/).

## Step 1: Install Jupyter
Open a terminal and run:
```bash
pip install jupyter
```
This installs Jupyter Notebook and JupyterLab.

## Step 2: Create a Workspace Directory
Create a dedicated folder for your Jupyter projects:
```bash
mkdir jupyter-workspace
cd jupyter-workspace
```

## Step 3: Launch Jupyter
Start Jupyter Notebook or JupyterLab:
- For Notebook: `jupyter notebook`
- For JupyterLab: `jupyter lab`

This opens a browser window at `http://localhost:8888` with the Jupyter interface.

## Step 4: Create Your First Notebook
In the Jupyter interface:
1. Click "New" > "Python 3" (or your kernel).
2. Name your notebook (e.g., `my_first_notebook.ipynb`).
3. Start writing code in cells.

## Step 5: Install Additional Packages (Optional)
For data science, install common libraries:
```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

## Step 6: Configure Jupyter (Optional)
Create a config file for custom settings:
```bash
jupyter notebook --generate-config
```
Edit `~/.jupyter/jupyter_notebook_config.py` to set options like password or port.

## Step 7: Use Extensions (Optional)
Install extensions for enhanced functionality:
```bash
pip install jupyter_contrib_nbextensions
jupyter contrib nbextension install --user
```

## Step 8: Run and Share
- Execute cells with Shift+Enter.
- Save notebooks as `.ipynb` files.
- Export to PDF/HTML via File > Download as.
