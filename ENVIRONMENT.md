## Environment Setup

### 1. Create a virtual environment

Ensure Python and `pip` are installed. Then run:

```bash
python -m venv venv
source venv/bin/activate
```

On Windows, activate it using:

```powershell
venv\Scripts\activate
```

### 2. Install dependencies

Install all dependencies listed in `requirements.txt`:

```bash
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

### 3. Generate or update `requirements.txt`

If you install additional packages or change package versions, update the dependency file using:

```bash
python -m pip freeze > requirements.txt
```

This records the installed packages and their versions so others can reproduce the Python environment.

### 4. Run the project

Activate the virtual environment and run the relevant Python script or notebook.

**Note:** The virtual environment itself (`venv/`) should not be committed to Git. Commit `requirements.txt` instead.
