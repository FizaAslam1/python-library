# NumPy Playbook (92 Lines)

A tiny, focused repo showcasing *NumPy* basics in ~92
lines of Python. Great as a quick-reference or a starting point for learners who want clean, wellâ€‘commented examples.

## âœ¨ Whatâ€™s inside
- Vector & matrix creation
- Elementwise ops, broadcasting
- Indexing, slicing, boolean masks
- Aggregations (sum, mean, argmax, etc.)
- Reshaping (reshape, ravel, transpose)
- Random utilities
- Small, readable script with docstrings

## ðŸ§° Requirements
- Python 3.9+
- NumPy (latest)


Advanced NumPy Concepts and Functions
📌 Introduction
This document covers essential advanced NumPy topics including:

Fancy Indexing

Broadcasting

Differences between NumPy array and Python list

Mathematical functions

Handling missing values

Plotting with NumPy

Key NumPy functions

✅ 1. Fancy Indexing
Fancy indexing allows passing an array of indices to access multiple elements at once.

python
Copy
Edit
import numpy as np

arr = np.array([10, 20, 30, 40, 50])
indices = [1, 3]
print(arr[indices])  # Output: [20 40]
✅ 2. Broadcasting
Broadcasting allows NumPy to perform operations on arrays of different shapes.

python
Copy
Edit
a = np.array([1, 2, 3])
b = 2
print(a + b)  # Output: [3 4 5]
✅ 3. NumPy Array vs Python List
Feature	Python List	NumPy Array
Performance	Slower	Faster (C-based)
Type Flexibility	Mixed types allowed	Same type only
Broadcasting	Not supported	Supported
Memory Usage	High	Low

✅ 4. Mathematical Formulas
python
Copy
Edit
a = np.array([1, 2, 3, 4])

print(np.sum(a))       # 10
print(np.mean(a))      # 2.5
print(np.std(a))       # Standard deviation
print(np.max(a))       # 4
print(np.min(a))       # 1
✅ 5. Handling Missing Values
python
Copy
Edit
a = np.array([1, 2, np.nan, 4])

print(np.nanmean(a))    # Mean ignoring NaN
print(np.isnan(a))      # Boolean array for NaNs
✅ 6. Plotting Graph (with matplotlib)
python
Copy
Edit
import matplotlib.pyplot as plt

x = np.linspace(0, 10, 100)
y = np.sin(x)

plt.plot(x, y)
plt.title('Sine Wave')
plt.show()
✅ 7. Important NumPy Functions
Function	Description
np.sort()	Sorts array
np.concatenate()	Joins arrays
np.append()	Appends values
np.flip()	Reverses elements
np.delete()	Deletes elements
np.clip()	Limits values within bounds
np.put()	Replaces values at specific indices
np.corrcoef()	Correlation coefficient
np.histogram()	Returns histogram data
np.cumsum()	Cumulative sum
np.percentile()	Percentile value
np.argmax()	Index of max value
np.argmin()	Index of min value

💡 Examples:
python
Copy
Edit
a = np.array([5, 1, 7, 3])
print(np.sort(a))         # [1 3 5 7]
print(np.flip(a))         # [3 7 1 5]
print(np.clip(a, 2, 6))   # [5 2 6 3]
print(np.cumsum(a))       # [5 6 13 16]
print(np.percentile(a, 50)) # Median = 5
📌 Summary
These advanced NumPy features are key for efficient numerical computing and data manipulation. Mastering them will help in:

Scientific computing

Machine learning

Data analysis

Statistical visualization



Install:
bash
python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux:
source .venv/bin/activate
pip install -U pip
pip install -r requirements.txt

requirements.txt (example):

numpy>=1.26


## ðŸš€ Run it
bash
python main.py

Or run a specific example if you split them:
bash
python examples/01_arrays.py


## ðŸ“‚ Project structure

.
â”œâ”€ main.py                # 81 lines of NumPy demos with comments
â”œâ”€ examples/              # (optional) split-out snippets
â”‚  â”œâ”€ 01_arrays.py
â”‚  â”œâ”€ 02_broadcasting.py
â”‚  â””â”€ 03_indexing.py
â”œâ”€ requirements.txt
â”œâ”€ README.md
â””â”€ LICENSE                # Choose MIT/Apache-2.0 or your preference


## ðŸ“ Suggested main.py outline
- Header docstring: what the script covers
- setup_demo() â€” create sample arrays
- show_*() functions â€” each prints a short, clear result
- if __name__ == "__main__": â€” call demos in order

Tip: keep each print small and annotated, e.g.
py
import numpy as np

a = np.arange(6).reshape(2, 3)
b = np.array([10, 20, 30])

print("a:\n", a)
print("b:", b)
print("a + b (broadcast):\n", a + b)


## âœ… Quick checks
Format & lint (optional but recommended):
bash
pip install black ruff
black .
ruff check .


## ðŸ§ª (Optional) Tests
If you add functions, include basic tests with pytest:
bash
pip install pytest
pytest -q


## ðŸ“¦ Badges (optional)
Add these to the top once you enable them:
- CI status (GitHub Actions)
- Code style: black
- License: MIT/Apache-2.0

## ðŸ¤ Contributing
PRs welcome! Keep examples concise & commented. One concept per snippet.

## ðŸ“„ License
MIT unless you prefer something else. Create a LICENSE file.

## ðŸ™‹ Support
Open an issue or discussion on GitHub.
