# Identity Collapse Detection Engine

A small diagnostic tool for measuring **identity drift, erosion, and collapse** in large language models.

It runs **iterative self-regeneration tests** on an Ollama-served model and detects when a synthetic writing identity becomes unstable or collapses.

This is **not a benchmark** and **not an alignment claim**.  
It is a **long-horizon stability diagnostic**.

---

## Features

- Iterative drift evaluation across N generations
- Soft vs. hard identity collapse detection
- Explicit drift causes (tone escalation, generic cadence, verbosity, etc.)
- ASCII compliance timeline (screenshot-friendly)
- Ranked drift-cause statistics
- Works with any Ollama model (default: `mistral`)
- Minimal dependencies (`requests` only)

---

## Quick Start

**Requirements**
- Python 3.9+
- Ollama installed
- One model pulled (recommended: `mistral`)

```bash
ollama pull mistral
pip install requests
python drift_evaluator.py
