<p align="center">
  <img src="assets/logo.png" width="120" alt="OpenForge logo" />
</p>

# OpenForge

**A community library of reinvented ML modules and algorithms — built from scratch, by developers.**

```bash
pip install openforge
```

---

## What Is This?

OpenForge is a public Python package where developers publish machine learning modules and algorithms they built themselves — from scratch, to learn, to experiment, to prove they could.

Not a fork. Not a wrapper. The real thing, hand-coded.

Scikit-learn already has Linear Regression. NumPy already has matrix operations. OpenForge doesn't care — if you built it yourself, it belongs here. This is a **museum of reinvented wheels**, and every wheel earns its place.

---

## How to Use It

Every contributor gets their own isolated namespace. No one's code can ever conflict with anyone else's.

```python
# Import a specific module
from openforge.ibrahim.markov_chains import model

# Import a specific function directly
from openforge.sarah.neural_net.layers import dense_layer

# Use it
result = model.predict(sequence)
```

The import path is always:
```
from openforge.<username>.<module_name> import <your_file>
```

---

## How to Contribute

Contributions are submitted through the **OpenForge web portal** — not via GitHub pull requests manually.

**Steps:**

1. Sign up at the OpenForge website
2. Write your module locally and zip the folder
3. Upload the zip through the portal
4. The system automatically validates your code, pushes it to this repo, and publishes it to PyPI

Your module is live on PyPI within minutes, with no manual review required — as long as it passes automated safety checks.

---

## What Gets Rejected

The automated validator scans every upload and rejects anything containing:

- `eval()` or `exec()` calls
- `subprocess` usage
- `os.system()` shell calls
- `pickle.loads()` or `marshal.loads()` deserialization
- `ctypes` usage
- `__import__()` dynamic imports
- Base64-encoded executable payloads
- Files that are not `.py`
- Zips exceeding 50MB total or 2MB per file

If your upload is rejected, you will see exactly which file and which pattern triggered the rejection.

---

## Rules

- **One namespace per account.** Your username folder belongs to you permanently.
- **Lowercase usernames only.** Letters, numbers, underscores. No spaces.
- **You can only touch your own folder.** Any PR that modifies another user's files is automatically closed.
- **No third-party dependencies** without a good reason. Pure Python and standard library preferred.
- **Working code only.** Broken modules that cannot be imported will be caught by CI and rejected.

---

## The Import Layout

```
openforge/
├── __init__.py
├── ibrahim/                     ← contributor namespace
│   ├── __init__.py
│   └── markov_chains/
│       ├── __init__.py
│       └── model.py
├── sarah/                       ← contributor namespace
│   ├── __init__.py
│   └── neural_net/
│       ├── __init__.py
│       └── layers.py
└── alex/                        ← contributor namespace
    ├── __init__.py
    └── linear_regression.py
```

---

## Tech Stack (for the curious)

| Layer | Technology |
|---|---|
| Package registry | PyPI (Trusted Publisher) |
| Source of truth | This GitHub repo |
| Upload portal | Vercel (static HTML/JS) |
| Auth + DB | Supabase |
| Code validation | Supabase Edge Functions (Deno) |
| CI / auto-merge | GitHub Actions |
| Versioning | Date-stamped: `0.YYYYMMDD.N` |

Every upload goes through: **portal → validator → GitHub PR → CI checks → auto-merge → version bump → PyPI publish**. No human in the loop.

---

## Version History

Versions follow the format `0.YYYYMMDD.N` where N increments if multiple releases happen on the same day.

Check the [Releases](https://github.com/Ibraheem5002/OpenForge/releases) page for the full history.

---

## License

MIT — do whatever you want with it.

---

*Built by Muhammad Ibrahim. Contributions welcome via the [OpenForge portal](https://openforge-web.vercel.app/).*
