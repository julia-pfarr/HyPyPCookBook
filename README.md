HyPyP Cookbook

**A community-driven onboarding kit for [HyPyP](https://github.com/ppsp-team/HyPyP) — the Hyperscanning Python Pipeline.**

This repository contains tutorials, documentation, and examples to help you go from "I installed HyPyP" to "I can run a complete synchrony workflow and understand what I'm doing."

---

## Quick Start

### 1. Install HyPyP

```bash
# Using pip
pip install hypyp

# Or using poetry (recommended for development)
git clone https://github.com/ppsp-team/HyPyP.git
cd HyPyP
poetry install
```

### 2. Clone this Cookbook

```bash
git clone https://github.com/ppsp-team/HyPyPCookbook.git
cd HyPyPCookbook
```

### 3. Run your first notebook

```bash
jupyter notebook notebooks/hello_synchrony.ipynb
```

---

## Brainhack Montreal 2026

This Cookbook was initiated during [Brainhack Montreal 2026][https://brainhack.org/](https://brainhackmtl.github.io/winter2026/).

### Project Goals

1. **Day 1 — Onboarding Kit Baseline**
   - Refreshed Quickstart
   - Cookbook skeleton
   - 5+ "good first issues"
   - Friction log (newcomer pain points)

2. **Day 2 — Tutorials End-to-End**
   - 2-3 runnable notebooks with saved outputs
   - Common pitfalls documentation
   - Unit tests for pipelines

3. **Day 3 — Demo-Ready Output**
   - Complete demo notebook (<10 min)
   - "How to contribute" guide
   - Summary report

### Pick an Issue

We have issues for all skill levels:

| Level | Issues |
|-------|--------|
| **Beginner** (no coding) | Documentation, glossary, friction testing |
| **Intermediate** (Python) | Notebooks, CI setup, pitfalls page |
| **Advanced** (engineering) | Stats rework, performance optimization, API fixes |

**[View all issues](https://github.com/ppsp-team/HyPyPCookbook/issues)**

---

## Contributing

We welcome contributions of all kinds! See [CONTRIBUTING.md](CONTRIBUTING.md) for:

- How to set up your environment
- How to submit a pull request
- Code style guidelines
- How contributions are credited

**First time contributing to open source?** Look for issues labeled [`good first issue`](https://github.com/ppsp-team/HyPyPCookbook/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22).

---

## Contributors

Thanks to everyone who has contributed to this Cookbook!

<!-- ALL-CONTRIBUTORS-LIST:START -->
| Name | Contributions |
|------|---------------|

<!-- ALL-CONTRIBUTORS-LIST:END -->

## Related Resources

- **HyPyP main repository:** https://github.com/ppsp-team/HyPyP
- **HyPyP paper:** [Frontiers article](https://www.frontiersin.org/articles/10.3389/fpsyg.2021.684813/full)
- **MNE-Python:** https://mne.tools/

---

## License

This project is licensed under the BSD 3-Clause License — see the [LICENSE](LICENSE) file for details.
