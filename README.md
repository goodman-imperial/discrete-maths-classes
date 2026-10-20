# Discrete Mathematics classes

Jupyter notebooks for the weekly classes of **Imperial College ELEC50006 (Discrete Mathematics)** by Dan Goodman.

Each notebook has the questions for one week's class, and some include starter code (in Python, and in C++ for weeks 1 and 3).

## Contents

| Week | Topic | Colab | Notebook |
| ---- | ----- | ----- | -------- |
| 1 | Intro and Fibonacci | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/goodman-imperial/discrete-maths-classes/blob/main/week-1-class.ipynb) | [week-1-class.ipynb](week-1-class.ipynb) |
| 2 | Complexity notation | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/goodman-imperial/discrete-maths-classes/blob/main/week-2-class.ipynb) | [week-2-class.ipynb](week-2-class.ipynb) |
| 3 | Divide and conquer | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/goodman-imperial/discrete-maths-classes/blob/main/week-3-class.ipynb) | [week-3-class.ipynb](week-3-class.ipynb) |
| 4 | Divide and conquer 2 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/goodman-imperial/discrete-maths-classes/blob/main/week-4-class.ipynb) | [week-4-class.ipynb](week-4-class.ipynb) |
| 5 | Dynamic programming | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/goodman-imperial/discrete-maths-classes/blob/main/week-5-class.ipynb) | [week-5-class.ipynb](week-5-class.ipynb) |
| 6 | Greedy algorithms | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/goodman-imperial/discrete-maths-classes/blob/main/week-6-class.ipynb) | [week-6-class.ipynb](week-6-class.ipynb) |
| 7 | Graphs (shortest paths, negative weights) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/goodman-imperial/discrete-maths-classes/blob/main/week-7-class.ipynb) | [week-7-class.ipynb](week-7-class.ipynb) |
| 8 | Various topics (parallel merge sort) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/goodman-imperial/discrete-maths-classes/blob/main/week-8-class.ipynb) | [week-8-class.ipynb](week-8-class.ipynb) |

## How to run the notebooks

You have two options:

- **Google Colab (easiest, nothing to install).** Click an "Open in Colab" badge above and sign in with a Google account. To keep your changes, use *File → Save a copy in Drive*.
- **On your own computer.** Follow the steps below. This works offline and lets you use your own editor.

### Running locally

This project uses [uv](https://docs.astral.sh/uv/) to manage Python and its packages. uv installs the right Python version and every package for you, so you don't need to install Python yourself.

**1. Install uv** (you only need to do this once):

```sh
# macOS / Linux
curl -LsSf https://astral.sh/uv/install.sh | sh

# Windows (PowerShell)
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

**2. Get the code:**

```sh
git clone https://github.com/goodman-imperial/discrete-maths-classes.git
cd discrete-maths-classes
```

**3. Install everything:**

```sh
uv sync
```

This creates a `.venv/` folder with Python 3.14 and the exact package versions listed in `uv.lock`.

**4. Start Jupyter:**

```sh
uv run jupyter lab
```

JupyterLab opens in your browser. Double-click a `week-N-class.ipynb` file to open it.

### Using VS Code instead

1. Run `uv sync` (step 3 above).
2. Install the **Python** and **Jupyter** extensions in VS Code.
3. Open the project folder and then a notebook.
4. Click **Select Kernel** (top right), choose *Python Environments*, then `.venv/bin/python` (on Windows, `.venv\Scripts\python.exe`).

## What's installed

| Package | Used for |
| ------- | -------- |
| `numpy` | Numerical arrays and timing experiments |
| `matplotlib` | Plotting (e.g. operation counts against input size) |
| `scipy` | Scientific computing helpers |
| `networkx` | Building and drawing graphs (week 7) |
| `jupyterlab`, `ipykernel` | Running the notebooks (dev only) |
| `ruff` | Linting and formatting Python code (dev only) |

## Common tasks

| I want to… | Command |
| ---------- | ------- |
| Add a package | `uv add <package>` |
| Remove a package | `uv remove <package>` |
| Update all packages to their latest versions | `uv lock --upgrade && uv sync` |
| Run a Python script | `uv run python my_script.py` |
| Check or format code | `uv run ruff check .` / `uv run ruff format .` |

You don't need to activate the virtual environment: `uv run` always uses the project's environment.

## C++ code (optional)

Weeks 1 and 3 also include C++ templates. Copy them into a `.cpp` file and compile with any C++17 compiler, for example:

```sh
g++ -std=c++17 -O2 solution.cpp -o solution && ./solution
```

On macOS, run `xcode-select --install` to get a compiler. On Windows, use [MSYS2](https://www.msys2.org/) or Visual Studio.

## Troubleshooting

- **`uv: command not found`**: restart your terminal after installing uv, so that it picks up the updated `PATH`.
- **The week 4 notebook stops with an `AssertionError`**: that cell is meant to fail. It shows what happens when an assertion is not satisfied.
- **The wrong kernel or missing packages in VS Code / Jupyter**: make sure you selected the `.venv` interpreter, then run `uv sync` again.

## License

GNU General Public License v2.0. See [LICENSE](LICENSE).
