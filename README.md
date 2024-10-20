# RAG
A step-by-step tutorial to build your own RAG model

1. Install Microsoft Visual Studio Code
2. Install Python Programming Language
3. Create a Free LLM Account
4. Paste Code
5. Run

## 1. Install Microsoft Visual Studio
### Step 1: Go to the Visual Studio Code Website
Open a web browser (e.g., Chrome, Firefox). Go to the official website: https://code.visualstudio.com/.
### Step 2: Download Visual Studio Code
On the homepage, you will see a "Download for Windows" button. Click this button.
If you're using Windows, the website will automatically detect your OS and suggest the correct download.
If you're using macOS or Linux, select the appropriate version for your system (Intel, ARM64, etc.).
The download should start automatically. If not, you can click the provided link to manually start the download.
### Step 3: Install Visual Studio Code on Windows
Once the download is complete, open the downloaded file (e.g., VSCodeUserSetup-x64.exe).
The installer will launch. Follow these steps:
Agree to the License Agreement: Click "I accept the agreement" and then click "Next."
Choose the installation location: The default location is fine, but you can change it if you prefer.
Select additional tasks:
It’s recommended to check options like "Add to PATH" for easier access.
You can also choose to create a desktop icon for quick access.
Click "Next" and then "Install."
Once installation is complete, click "Finish" to launch Visual Studio Code.

## 2. Install Python Programming Language
### Step 1: Install Python
Go to the Python website: Visit the official Python website at https://www.python.org/downloads/.
Download the latest version of Python: The website should automatically detect your operating system (Windows, macOS, Linux). Click the "Download Python" button for your platform.
Open the downloaded .exe file.
Check the box that says "Add Python to PATH". This is crucial as it allows you to run Python from the command line.
Click "Install Now."
### Step 2: Install Python Extension in VS Code
Open VS Code.
Install the Python extension:
Click on the Extensions icon on the left sidebar or press Ctrl+Shift+X (Windows/Linux) or Cmd+Shift+X (macOS).
Search for Python in the Extensions Marketplace.
Install the extension from Microsoft (it should have high ratings).

## 3. Install dependencies
### Option 1: pip install all dependencies one by one
Dependencies are included in the `pyproject.toml` file under the `[tool.poetry.dependencies]` header, you can open your terminal and just type `pip install <name_of_package>` for example `pip install openai` make sure you install the specific versions described in the `pyproject.toml` file

### Option 2: manage dependencies through poetry

# Poetry Installation and Dependency Management
This guide will walk you through installing Poetry and managing dependencies in a Python project using the `pyproject.toml` file.

## Step 1: Install Poetry
Poetry is a Python package manager that simplifies dependency management and package building.

### 1.1 Install via the Official Installer
Run the following command to download and install Poetry:

```bash
curl -sSL https://install.python-poetry.org | python3 -
```

On Windows, you can use PowerShell:

```bash
(Invoke-WebRequest -Uri https://install.python-poetry.org -UseBasicParsing).Content | python -
```

### 1.2 Verify the Installation
Once installed, verify that Poetry is working by checking the version:

```bash
poetry --version
```

## Step 2: Add Poetry to Your Path (if necessary)
If Poetry is not automatically added to your `PATH`, you'll need to do it manually.

### 2.1 Find the Path
Poetry is usually installed in `~/.local/bin` on macOS/Linux or `%USERPROFILE%\.poetry\bin` on Windows.

### 2.2 Add to Path
- **macOS/Linux**: Add the following line to your shell configuration file (e.g., `~/.bashrc`, `~/.zshrc`):

  ```bash
  export PATH="$HOME/.local/bin:$PATH"
  ```

- **Windows**: Add the Poetry path to your system environment variables through the Control Panel.

## Step 3: Navigate to Your Project Directory
Navigate to the directory containing the `pyproject.toml` file:

```bash
cd /path/to/your/project
```

Make sure that the `pyproject.toml` file is in this directory.

## Step 4: Install Project Dependencies Using Poetry
To install all dependencies from the `pyproject.toml` file, run:

```bash
poetry install
```

Poetry will resolve the dependencies, create a virtual environment, and install everything needed for your project.

### 4.1 Activate the Virtual Environment (Optional)
If you want to activate the virtual environment that Poetry created, use:

```bash
poetry shell
```

### 4.2 Verify the Installation
To check the installed dependencies, use:

```bash
poetry show
```

## Step 5: Adding or Removing Dependencies (Optional)
If you need to manage dependencies after installation:

### 5.1 Add a Dependency
To add a new dependency, run:

```bash
poetry add <package-name>
```

### 5.2 Remove a Dependency
To remove a dependency, run:

```bash
poetry remove <package-name>
```

## Step 6: Running Python Scripts
With dependencies installed, you can run your Python scripts inside the Poetry-managed virtual environment.

- If you're in a Poetry shell, use:

  ```bash
  python your_script.py
  ```

- If you're not in the Poetry shell, run:

  ```bash
  poetry run python your_script.py
  ```

## Step 7: Locking Dependencies (Optional)
To manually update the `poetry.lock` file after modifying dependencies:

```bash
poetry lock
```

This ensures the lock file is up to date with the latest dependencies.
