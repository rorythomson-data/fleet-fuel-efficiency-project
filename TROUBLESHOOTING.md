# 🛠️ Troubleshooting Log – Fleet Fuel Efficiency Project

This is a personal log of issues I encountered during setup and early development of this project. It includes context, the problems, and the solutions I applied. The goal is to help me avoid similar pitfalls in future projects and remember how I solved them.

---

## 1. PowerShell Blocked Script Activation

**Context:**  
I created a virtual environment using `python -m venv venv` and tried to activate it from the VS Code terminal (PowerShell).

**Issue:**  
PowerShell blocked the activation script with an error about execution policies:
```
venv\Scripts\activate : running scripts is disabled on this system
```

**Solution:**  
I opened a new terminal and selected **Command Prompt** instead. From there, I ran:
```bash
venv\Scripts\activate
```
This successfully activated the environment without needing to change PowerShell settings.

---

## 2. Unsure if I Created a Valid Jupyter Notebook

**Context:**  
I created a notebook via VS Code’s “New File → Notebook” option and wasn’t sure if it was a real `.ipynb` file.

**Issue:**  
I wasn’t sure if this was Jupyter-compatible.

**Solution:**  
Confirmed that it saved as a `.ipynb` file and opened with full notebook features (cell execution, kernel selection, Markdown cells). Verified this by checking file extension and notebook toolbar.

---

## 3. No Jupyter Kernel Selected

**Context:**  
When opening the notebook for the first time, it asked me to select a kernel.

**Issue:**  
The kernel for my virtual environment didn’t show up automatically.

**Solution:**  
Used `Ctrl+Shift+P` to open the Command Palette → Chose `Python: Select Interpreter` → Selected:
```
Python 3.13.0 ('venv')
```
Then returned to the notebook and clicked “Select Kernel” to use the same interpreter.

---

## 4. ipykernel Package Missing

**Context:**  
I tried running a cell in the notebook after selecting the kernel.

**Issue:**  
Got a VS Code message:
```
Running cells with Python 3.13.0 ('venv') requires the ipykernel package
```

**Solution:**  
Clicked **Install** in the popup. VS Code installed `ipykernel` inside the virtual environment.

---

## 5. pandas Not Installed

**Context:**  
Ran:
```python
import pandas as pd
```
to load and check the dataset.

**Issue:**  
Got:
```
ModuleNotFoundError: No module named 'pandas'
```

**Solution:**  
Ran this in the terminal (which was already inside the activated `venv`):
```bash
pip install pandas matplotlib seaborn
```
After that, I was able to import pandas and run cells successfully.

---

## 6. Wanted to Be Sure Project Looked Professional

**Context:**  
As I set up the structure, I wanted to avoid doing anything amateurish (e.g., committing the `venv/` folder or having unclear documentation).

**Issue:**  
Uncertainty about folder layout, Git hygiene, and clarity of README/structure.

**Solution:**  
- Created a `.gitignore` to exclude `venv/`, `__pycache__/`, and `.ipynb_checkpoints/`
- Added a `README.md` with background and purpose
- Added a `PROJECT_LOG.md` to document progress
- Verified that my notebooks and structure followed common best practices

---

## 7. Handling of Personal Project Details

**Context:**  
Since `PROJECT_LOG.md` is public and `TROUBLESHOOTING.md` is private, I wanted to make sure more personal details are included in the latter.

**Personal Content**:  
- Discussed **setup challenges** and technical issues faced.
- Noted how certain configurations (like `venv/` and `.gitignore`) needed specific adjustments for the project to run smoothly.

---

## ✅ Summary

Despite a few hiccups, I now:
- Have a working virtual environment
- Can run Jupyter notebooks using my own kernel
- Have key packages installed
- Am following best practices with structure, Git, and documentation
