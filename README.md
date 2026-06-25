# OpenForge

Welcome to **OpenForge**! This is a public Python library built for developers who love to build things from scratch. 

Have you ever spent days coding a custom Linear Regression algorithm, a unique Markov Chain module, or a custom game engine just to learn how it works under the hood? You can't merge it into major libraries like Scikit-Learn because they already have it—but your hard work shouldn't be wasted. 

This library is a **museum of reinvented wheels**. It is a place to publish your custom-built modules, showcase your engineering grit, and leave your permanent mark on the open-source world.

---

## 🛠️ How It Works (The Import Layout)

To prevent anyone's code from overwriting someone else's, every single developer gets their own isolated **username space**. Users can import your exact code using this clean layout:

```python
# If your username is 'alex' and you built a tictactoe bot
from artisan_wheelhouse.alex import infinite_tictactoe

# If your username is 'sarah' and you organized your ML modules
from artisan_wheelhouse.sarah.ml.supervised import linear_regression
```

---

## 📜 The Rules for Publishing

Anyone is welcome to contribute! To keep the library clean, functional, and organized, all submissions must follow these simple rules:

1. **Anyone Can Publish:** Whether you are a computer science student or a senior engineer, if you built something from scratch to learn, you can submit it.
2. **Unique Usernames:** Your username folder must be completely unique. Once a username is taken, it belongs to that developer.
3. **Username Format:** Your username folder name must be **all lowercase** and contain **no spaces** (use underscores if needed, e.g., `john_doe`). It must be a valid Python identifier.
4. **Strict Boundaries:** You can only add or modify files inside your own specific username folder. Touching or modifying another user's folder will result in immediate rejection.
5. **The `__init__.py` Requirement:** Every folder and sub-folder you create inside your namespace **must** contain an `__init__.py` file so Python can find and import your modules correctly.
6. **Honest & Working Code:** Your module must do exactly what it claims to do. It will be carefully reviewed. If it contains game-breaking bugs, malicious code, or does not work as advertised, it will be rejected.
7. **Keep Dependencies Low:** Try to use vanilla Python or basic standard libraries. If your module requires heavy external packages, explain why in your pull request.

---

## 🚀 How to Submit Your Module

1. **Fork** the repository on GitHub.
2. Create your unique username folder under `artisan_wheelhouse/` (e.g., `artisan_wheelhouse/your_username/`).
3. Add an empty `__init__.py` file inside your folder.
4. Write your beautiful code, organize it into categories if you like, and include a short docstring explaining how to use it.
5. Open a **Pull Request (PR)**. Once reviewed and merged, your code will be bundled into the next official PyPI release for everyone to `pip install`!

*Let's build, reinvent, and leave a mark!*
