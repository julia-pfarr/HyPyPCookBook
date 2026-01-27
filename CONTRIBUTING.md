# Contributing to HyPyP Cookbook

Thank you for your interest in contributing! This guide will help you get started, whether you're joining us at Brainhack Montreal or contributing remotely.

---

## 📋 Table of Contents

1. [Code of Conduct](#code-of-conduct)
2. [Getting Started](#getting-started)
3. [How to Contribute](#how-to-contribute)
4. [Brainhack Sprint Guide](#brainhack-sprint-guide)
5. [Pull Request Process](#pull-request-process)
6. [Style Guidelines](#style-guidelines)
7. [Getting Help](#getting-help)
8. [Credit & Attribution](#credit--attribution)

---

## Code of Conduct

This project follows the [Brainhack Code of Conduct](https://docs.google.com/document/d/11aE6vv67i9pzOUN7DTypqiAVUutXAijP7_jZTURHhAM/edit?tab=t.0#heading=h.4eiasrosux9m). Please read it before participating. We are committed to providing a welcoming and inclusive environment for everyone.

**In short:** Be respectful, be kind, be collaborative.

---

## Getting Started

### Prerequisites

- Python >= 3.10, < 3.14
- Git
- A GitHub account

### Setup your environment

```bash
# 1. Fork this repository on GitHub, then clone your fork
git clone https://github.com/YOUR_USERNAME/HyPyPCookbook.git
cd HyPyPCookbook

# 2. Add the upstream remote
git remote add upstream https://github.com/ppsp-team/HyPyPCookbook.git

# 3. Create a virtual environment (recommended)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# 4. Install dependencies
pip install -r requirements.txt
# 5. Verify installation
python -c "import hypyp; print('HyPyP version:', hypyp.__version__)"
```

### Verify everything works

```bash
# Run the test suite
pytest tests/

# Launch Jupyter to explore notebooks
jupyter notebook notebooks/
```

---

## How to Contribute

### Types of contributions we're looking for

| Type | Examples | Labels |
|------|----------|--------|
| **Documentation** | Improve README, add glossary terms, fix typos | `documentation` |
| **Tutorials** | Write notebooks, add examples, improve explanations | `tutorial` |
| **Bug reports** | Found something broken? Let us know! | `bug` |
| **Features** | New functionality, API improvements | `enhancement` |
| **Tests** | Unit tests, integration tests, CI | `tests` |
| **Review** | Review pull requests from others | |

### Finding something to work on

1. **Check the issues:** Look for issues labeled [`good first issue`](https://github.com/ppsp-team/HyPyPCookbook/issues?q=label%3A%22good+first+issue%22) or [`help wanted`](https://github.com/ppsp-team/HyPyPCookbook/issues?q=label%3A%22help+wanted%22)

2. **Claim an issue:** Comment on the issue saying you'd like to work on it

3. **No matching issue?** Open a new one to discuss your idea before starting work

---

## Brainhack Sprint Guide

### Day-by-day schedule

#### Day 1 — Onboarding Kit Baseline

| Time | Activity |
|------|----------|
| 11:00-12:00 | **Kick-off**: introductions, setup, role distribution |
| 13:00-14:30 | **Sprint #1**: Installation testing (beginners) / Cookbook skeleton (intermediate+) |
| 14:30-15:00 | **Sync**: Share friction points |
| 15:00-16:30 | **Sprint #2**: Friction fixes / Good first issues creation |
| 16:30-18:00 | **Unconference** (optional): Git basics, HyPyP intro |

#### Day 2 — Tutorials End-to-End

| Time | Activity |
|------|----------|
| 9:00-10:00 | **Stand-up**: Day 1 recap, notebook assignments |
| 10:00-12:00 | **Sprint**: Write notebooks |
| 13:00-15:30 | **Sprint**: Continue notebooks + tests |
| 15:30-16:30 | **Sync**: Test notebooks, merge PRs |

#### Day 3 — Demo-Ready Output

| Time | Activity |
|------|----------|
| 9:00-10:00 | **Sprint**: Finalize docs and demo notebook |
| 10:00-11:00 | **Unconference** (optional): Lessons learned, how to continue |
| 11:00-12:00 | **Test & prep**: Final testing, prepare presentation |
| 13:00-15:00 | **Polish**: Last fixes, contributor credits |
| 15:00-17:00 | **Wrap-up presentations** |

### Issue assignment by level

| Level | Recommended Issues |
|-------|-------------------|
| **Beginner** | B1 (Installation), B2 (Glossary), B3 (Friction log), B4 (Docstrings) |
| **Intermediate** | I1 (Simulated data), I2 (Pitfalls), I3 (CI), I4 (Tests) |
| **Advanced** | A1 (Stats rework), A2 (Performance), A3 (API fix), A4 (Wrapper) |

### Tips for a successful sprint

- **Start with a small PR** — even a typo fix counts!
- **Open draft PRs early** — get feedback before you're done
- **Document as you go** — notes help others continue your work
- **Ask questions** — no question is too basic
- **Take breaks** — attend TrainTracks, socialize, rest

---

## Pull Request Process

### 1. Create a branch

```bash
# Update your fork
git fetch upstream
git checkout main
git merge upstream/main

# Create a feature branch
git checkout -b feature/your-feature-name
# Examples:
# git checkout -b docs/glossary-page
# git checkout -b tutorial/hello-synchrony
# git checkout -b fix/installation-macos
```

### 2. Make your changes

- Write clear commit messages
- Keep commits focused (one change per commit)
- Add tests if applicable

### 3. Push and open a PR

```bash
git push origin feature/your-feature-name
```

Then open a Pull Request on GitHub. Use this template:

```markdown
## Description
Brief description of what this PR does.

## Related Issue
Closes #XX

## Type of change
- [ ] Documentation
- [ ] Tutorial
- [ ] Bug fix
- [ ] New feature
- [ ] Tests

## Checklist
- [ ] I have read the CONTRIBUTING.md guide
- [ ] My code follows the style guidelines
- [ ] I have tested my changes
- [ ] I have updated documentation if needed
```

### 4. Code review

- A maintainer will review your PR
- Address feedback by pushing new commits
- Once approved, your PR will be merged!

---

## Style Guidelines

### Python code

- Follow [PEP 8](https://peps.python.org/pep-0008/)
- Use type hints where possible
- Write docstrings in [NumPy style](https://numpydoc.readthedocs.io/en/latest/format.html)

```python
def compute_something(data: np.ndarray, n_epochs: int = 10) -> np.ndarray:
    """
    Compute something useful.

    Parameters
    ----------
    data : np.ndarray
        Input data with shape (n_channels, n_samples).
    n_epochs : int, optional
        Number of epochs. Default is 10.

    Returns
    -------
    np.ndarray
        Output data with shape (n_epochs, n_channels).

    Examples
    --------
    >>> result = compute_something(data, n_epochs=5)
    """
    pass
```

### Notebooks

- Clear narrative flow with markdown explanations
- Run all cells before committing (outputs saved)
- Keep runtime reasonable (<10 min for tutorials)
- Include "What you'll learn" at the top
- Include "What to check if something looks wrong" sections

### Documentation

- Use clear, simple language
- Explain jargon (or link to glossary)
- Include examples where possible
- Use proper Markdown formatting

---

## Getting Help

- **During Brainhack:** Ask in the project room or on our communication channel
- **GitHub issues:** Open an issue with the `question` label

Don't hesitate to ask! There are no silly questions.

---

## Credit & Attribution

We believe in recognizing all contributions, not just code.

### How we credit contributors

1. **GitHub:** Your commits and PRs are automatically tracked
2. **README:** Contributors are listed with contribution types
3. **Presentations:** Brainhack wrap-up will acknowledge all participants

### Contribution types we recognize

| Type | Description |
|------|-------------|
| Code | Writing code, scripts |
| Documentation | README, guides, docstrings |
| Tutorials | Jupyter notebooks, examples |
| Design | Figures, diagrams, visualizations |
| Ideas | Proposing features, discussions |
| Infrastructure | CI/CD, tooling, deployment |
| Tests | Writing tests |
| Review | Reviewing PRs |
| Bug reports | Reporting issues |
| Questions | Asking helpful questions |

### Adding yourself to the contributors list

After your first contribution is merged, add yourself to the README:

```markdown
| Your Name |
```

Or ask a maintainer to add you!

---

## Thank You!

Every contribution, no matter how small, helps make HyPyP more accessible to the community. Thank you for being part of this project!
