# Module 0: Setup & Tools

> **Before diving into the world of AI, take a moment to set your foundation — not just for learning, but because this is the path you’ve chosen to explore, build, and create.**
> 
> This module is your compass. It will help you set up an environment that’s clean, reproducible, and scalable. These good practices will save you *time*, reduce *technical debt*, and allow you to grow smoothly as you dive deeper into AI/ML.
>
> **Think of this as a checklist you’ll keep coming back to.** Some things here may seem advanced at first — that’s okay. As you start creating more complex projects, you’ll revisit these concepts and truly appreciate having started right.

---

## Module Outline

- [1. Step Up: Python, VSCode, + Useful Extensions](#1-step-up-python-vscode--useful-extensions)
- [2. Environment Good Practices: Conda & Pip](#2-environment-good-practices-conda--pip)
- [3. AI Tools for Productivity](#3-ai-tools-for-productivity)
- [4. Version Control: Git & GitHub](#4-version-control-git--github)
- [5. Project Structure & Organization](#5-project-structure--organization)
- [6. Terminal Basics](#6-terminal-basics)

---

## 1. Step Up: Python, VSCode, + Useful Extensions

Before writing any code, let’s get your tools ready. Python is the heart of modern ML. VSCode is your go-to editor.

### 🔹 Install Python

- 📥 [Download Python](https://www.python.org/downloads/)
- Recommended: Python **3.10+**
- ✅ During installation, **check “Add Python to PATH”** — this makes it accessible from your terminal.

Check the installation:

```bash
python --version
```

---

### 🔹 Install VSCode

- 📥 [Download VSCode](https://code.visualstudio.com/)
- Lightweight, fast, and powerful — with built-in support for Python, Jupyter, and Git.

Recommended VSCode Extensions:

| Extension             | Why it matters                                  |
|-----------------------|--------------------------------------------------|
| Python (by Microsoft) | Essential Python support                        |
| Jupyter               | Run notebooks inside VSCode                     |
| Pylance               | Fast, intelligent autocomplete and type checking|
| GitLens               | See Git history and diffs easily               |
| Auto Rename Tag       | Helps when editing HTML/JSX                    |
| Prettier              | Auto-format your code consistently              |
| GitHub Copilot, Cursor, Codeium | AI coding assistants                  |

---

## 2. Environment Good Practices: Conda & Pip

> **Why environments matter:** Without isolation, different projects can conflict and break each other. A clean Python environment means reproducibility, portability, and peace of mind.

**What is a Python Environment?**

An **environment** is a sandbox — a separate space with its own Python version and libraries. This way, dependencies don’t clash between projects.

**Why one environment per project?**

- Keeps things organized  
- Makes your project portable and shareable  
- Easier to deploy, debug, or upgrade  

**What is a Python Library?**

A **library** is a collection of pre-written code (functions, classes, tools) that you can use in your own projects — instead of writing everything from scratch.

Examples:

- `numpy` for math and arrays  
- `pandas` for data analysis  
- `matplotlib` for plots and charts  
- `requests` for making web requests  

**Why are libraries useful?**

- **Save time:** You don’t have to reinvent the wheel  
- **Boost productivity:** Let experts handle the tricky stuff  
- **Improve code quality:** Libraries are usually well-tested and optimized  
- **Enable complex features:** Like machine learning or image processing  

> ⚠️ You **need** libraries because most real-world tasks would be too complex, slow, or error-prone without them.

---

### 🔹 Install Conda

Choose one of the following:

- 📥 [Miniconda](https://docs.conda.io/en/latest/miniconda.html): Lightweight
- 📥 [Anaconda](https://www.anaconda.com/products/distribution): Comes with most data science packages

**Create & Use a Conda Environment**

```bash
cd project (your own path of the project)
conda create -n myproject python=3.10
conda activate myproject
```

You now have a clean environment called `myproject`.

---

### 🔹 Install Python Packages

Install packages *inside* your environment:

```bash
pip install pandas numpy matplotlib scikit-learn
```

---

### 🔹 Manage Installed Packages

Check which packages are currently installed:

```bash
pip list
```

Upgrade a specific package (e.g. pandas):

```bash
pip install --upgrade pandas
```

Uninstall a package:

```
pip uninstall matplotlib
```

> 💡 Tip: Use pip show <package> to get details like version, install location, and dependencies.

---

#### 🔹 Save Dependencies to `requirements.txt`

```bash
pip freeze > requirements.txt
```

To install them later:

```bash
pip install -r requirements.txt
```

> 📁 Put `requirements.txt` in the **root of your project**. It’s your project's memory of what it needs to run.

** Why use `requirements.txt`?**

A `requirements.txt` file lists all the Python libraries your project depends on — including their exact versions.

**Benefits:**

- **Reproducibility**: Teammates or servers can install *exactly* what your code needs  
- **Portability**: Others can run your project without guessing or Googling missing packages  
- **Deployment-ready**: Perfect for deploying apps to the cloud or production environments  
- **Version control**: You know which version of a library you used, which avoids future bugs  

> 🧠 Think of it as a snapshot of your Python environment at a given time.

---

## 3. AI Tools for Productivity

AI can boost your productivity — but don’t lose your critical thinking.

**Use These Tools to Work Smarter:**

- GitHub Copilot  
- Cursor (AI-first IDE)  
- Codeium  
- ChatGPT  
- Tabnine  

These tools can:  
- Speed up boilerplate code  
- Help debug  
- Suggest patterns  

> 🧠 **Think before you paste.** Don’t blindly accept AI code — read, understand, and adapt it. These tools are your co-pilot, not your autopilot.

**Why Use AI Tools?**

AI tools are **very important** if you want to stay up to date and maximize your productivity. They help you learn faster, write code more efficiently, and explore new ideas. However, recent research shows that over-reliance on AI assistants like ChatGPT can lead to *cognitive under-engagement* and lower critical thinking skills over time.  

A study from 2025 ([Kosmyna et al., arXiv:2506.08872](https://arxiv.org/abs/2506.08872)) found that:

- Users relying heavily on AI showed decreased brain connectivity related to active thinking  
- They struggled with memory recall and ownership of their work  
- Over months, excessive use without critical engagement may impair learning and performance  

> 🔍 **Bottom line:** Use AI tools as a powerful aid — but stay actively engaged and think critically. Balance is key for long-term growth.

---

## 4. Version Control: Git & GitHub

> Version control = time machine for your code.

**What is Git?**

A **version control system** to track and save every change in your code.

**What is GitHub?**

A **cloud platform** to host and collaborate on your Git repositories.

---

### 🔹 Basic Git Workflow

```bash
git init                     # Start Git in your folder
git add .                    # Stage all files
git commit -m "Initial commit"  # Save the snapshot
```

---

### 🔹 Push Your Code to GitHub

```bash
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
git branch -M main
git push -u origin main
```

---

### 🔹 Add a `.gitignore` File

A `.gitignore` tells Git what not to track (usefull to not upload heavy files or sensible ones). Example:

```bash
__pycache__/
*.ipynb_checkpoints
*.log
.env
venv/
*.pkl
*.h5
.DS_Store
```

> 📄 Use [gitignore.io](https://www.toptal.com/developers/gitignore) to generate a `.gitignore` file tailored to Python, Jupyter, etc.

---

## 5. Project Structure & Organization

### 🔹 Basic project Structure

> Clean structure = faster navigation, easier debugging, and scalable growth.

Here’s a good starting point:

```bash
my_project/
├── data/               # Raw and processed data
├── notebooks/          # Jupyter notebooks for experiments (.ipynb)
├── models/             # Saved model files (e.g. .pkl, .h5)
├── src/                # Python source code
│   └── utils.py
├── requirements.txt    # Project dependencies
├── environment.yml     # (Optional) Conda environment config
├── .gitignore          # Git ignore rules
└── README.md           # Project description & usage
```

---

### 🔹 Modular Code & `__init__.py`

Split code into small, reusable modules for clarity and testing.

`__init__.py` makes a folder a package, enabling imports like `from src import utils`.

Example folder structure and import example:
```bash
src/
├── __init__.py
├── utils.py
```
Import example:

`from src import utils`

---

### 🔹 Clean Entry Point & Configuration
Keep your main application entry point (e.g., `main.py`) separate. This file should handle program startup and orchestrate module usage.

Organize other functionality into separate `.py` files/modules inside `src/` or similar folders to keep your code modular, clean, and well documented.

This approach makes the codebase easier to maintain and test.

When a Python file is run, Python sets a special variable called `__name__`.

- If the file is run **directly** (`python main.py`), `__name__ == "__main__"`  
- If the file is **imported**, `__name__` will be the name of the module (e.g. `"main"`)

This block:

```python
if __name__ == "__main__":
    main()
```

---

### 🔹 Optional: CLI & Configuration Files
You can add a Command Line Interface (CLI) module (e.g., using [`argparse`](https://docs.python.org/3/library/argparse.html)) to handle user input options and flags.

Use configuration files like YAML ([`config.yaml`](https://python.land/data-processing/python-yaml)) or `JSON` to store environment-specific settings, parameters, or secrets — keeping code flexible and easier to configure without changing code.

Example config file location:

```bash
config/
└── config.yaml
```

This separation enhances portability, reusability, and makes your project production-ready.

---

## 6. Terminal Basics

> You’ll spend a lot of time in the terminal. Knowing a few commands saves a ton of clicks.

```bash
cd my_folder           # Navigate into a folder
ls                     # List files and folders
mkdir new_folder       # Create a new folder
python script.py       # Run a Python script
conda activate my_env  # Activate your Conda environment
git status             # See what has changed in Git
```

---

### 💡 Final Thought

Before diving into models and datasets, take the time to **set up your system well**. This guide is something you’ll come back to *again and again*.

You might not need everything today, but as you grow and start building real projects, this setup will save you **countless hours**.

> 📌 **Come back to this. Review it often. It’s your toolbox.**

