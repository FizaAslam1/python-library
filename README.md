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
