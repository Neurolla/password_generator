# 🔐 Password Generator Dashboard

An interactive **web application** built with **Python** and **Streamlit** that lets you generate secure passwords quickly and easily.
You can choose between three password types — **Random**, **Memorable**, and **PIN Code** — and customize them based on your preferences.

---

## 🧩 Project Structure

```
password-generator-dashboard/
│
├── app.py                      # Streamlit web app interface
├── password_generators.py      # Password generator classes
├── requirements.txt            # Project dependencies
└── README.md                   # Documentation (this file)
```

---

## ⚙️ Requirements

* Python **3.8+**
* Streamlit
* NLTK (Natural Language Toolkit)

Install all required packages using the `requirements.txt` file:

```bash
pip install -r requirements.txt
```

Or install them manually:

```bash
pip install streamlit nltk
```

Then, open a Python shell and download the NLTK *words* dataset:

```python
import nltk
nltk.download('words')
```

---

## ▶️ Running the Project

To start the Streamlit app, run:

```bash
streamlit run app.py
```

This will automatically open a browser window on your local server (usually at
[http://localhost:8501](http://localhost:8501)).

From the sidebar, choose the password type and settings you prefer, then click **Generate** to create your password.

---

## ✨ Features

* Choose from **Random**, **Memorable**, or **PIN** password types
* Adjustable password **length** (6–64 characters)
* Include or exclude **uppercase**, **lowercase**, **digits**, and **symbols**
* Option to **avoid ambiguous characters** (e.g., I, l, 1, O, 0)
* **Memorable mode:** create passwords from real words, with customizable separator and capitalization
* **PIN mode:** numeric code with configurable length
* Displays estimated **password entropy** (strength)
* Keeps a short **password history** and allows clearing it

---

## 🧠 Code Overview

### `password_generators.py`

Contains all generator classes:

* `PasswordGenerator` – abstract base class
* `RandomPasswordGenerator` – generates random character passwords
* `MemorablePasswordGenerator` – generates easy-to-remember word-based passwords
* `PinCodeGenerator` – generates numeric PIN codes

### `app.py`

Implements the **Streamlit** interface:

* Sidebar for password settings
* Generate button and password display
* Entropy calculation and strength indicator
* Optional history of previously generated passwords

---

## 💡 Example Output

```text
[Random] length=16
→ Entropy ≈ 100.3 bits → Strength: strong

[Memorable] words=4, separator="-"
→ RIVER-DREAM-SUGAR-CLOUD

[PIN] length=6
→ 492781
```

## 🗺 Roadmap

* [ ] Add **Copy to Clipboard** button
* [ ] Add **Download passwords** as `.txt`
* [ ] Save user preferences in session state
* [ ] Add **unit tests** with GitHub Actions CI

---

## 👩🏼‍💻 Author

**Vida 🍀**
Passionate about building simple, elegant tools with Python and exploring Cognitive Science.
📍 [GitHub Profile](https://github.com/Neurolla)

