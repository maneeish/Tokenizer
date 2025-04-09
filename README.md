# 🧩 Tokenizer Web App

A lightweight, browser-based tokenizer tool built with HTML, CSS, and JavaScript. It takes input text, breaks it down into tokens, counts characters, and generates simulated token IDs using a hash function.

Screenshots

<img width="960" alt="Screenshot 2025-04-09 182022" src="https://github.com/user-attachments/assets/826f0f3d-d5cf-4e48-a967-37060bb7715e" />


## 🔗 Demo
https://tokenizergenerator.netlify.app/

## ✨ Features

- Simple, responsive UI
- Tokenizes text based on a smart regex
- Displays:
  - Total number of tokens
  - Character count
  - Simulated Token IDs
- No dependencies or frameworks needed

---

## 📦 Getting Started

### 🔧 Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/tokenizer.git
   cd tokenizer-app
   ```

2. Open `index.html` in your browser:
   ```bash
   open index.html
   ```
   *(or double-click the file if you're on Windows)*

---

## 📁 Project Structure

```
tokenizer-app/
├── index.html         # Main HTML file containing the complete app
├── README.md          # Project documentation
└── screenshot.png     # Optional screenshot for GitHub preview
```

---

## 🧮 How It Works

- **Tokenization Regex:**
  ```js
  const tokens = text.match(/\b\w+\'?\w*|\S/g) || [];
  ```
- **Token ID Generator:**
  ```js
  function simulateTokenId(token) {
    let hash = 0;
    for (let i = 0; i < token.length; i++) {
      hash = (hash * 31 + token.charCodeAt(i)) % 100000;
    }
    return hash;
  }
  ```

---

## 🤝 Contributing

Contributions are welcome! Here's how:

1. Fork the repo
2. Create a new branch: `git checkout -b feature-name`
3. Commit your changes: `git commit -m "Add feature"`
4. Push to the branch: `git push origin feature-name`
5. Open a Pull Request

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 🙌 Acknowledgements

Inspired by tokenizer concepts used in NLP and LLMs.

