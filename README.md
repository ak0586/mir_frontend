# Math Information Retrieval System Frontend (Flutter)

A new Flutter project.

This is the **Flutter's frontend** for the Math Search Engine project. It allows users to input LaTeX or mathematical expressions, submit search queries, and view HTML+MathML documents. This frontend works seamlessly on **Android APK** and **Web browsers**.

---

## ✨ Features

* 🔍 Search LaTeX or math expressions
* 📄 Renders HTML with MathML correctly on both Android and Web
* 💡 Uses `WebView` for Android, and iframe for MathJax on Web
* ⏱ Shows response time and result count
* ✅ Clean UI with animation, loading indicators, and error handling

---

## 🚀 How It Works

1. User types a LaTeX or math query.
2. Query is converted to JSON-compatible format.
3. Sent to backend via POST `/search`.
4. Results are listed. Tapping a result opens a new page:

   * **Web**: Opens via `HtmlElementView` (iframe with MathJax rendering)
   * **Mobile**: Opens using `WebViewController` with MathJax injected

---

## 📁 Key Files

* `main.dart` — Main search UI and routing logic
* `mobile_html_viewer.dart` — Renders HTML using WebView for Android
* `web_html_viewer.dart` — Renders HTML using iframe for Web

---

## 🛠 Setup Instructions

### Prerequisites

* Flutter SDK installed
* Backend running on `http://127.0.0.1:8000` (API must be active)

### Run on Web

```bash
flutter run -d chrome
```

### Run on Android Emulator

```bash
flutter run -d emulator-5554
```

> The app will automatically switch between Web and Mobile renderers.

---

## 📌 Notes

* HTML returned from backend **must contain MathML**.
* No external styling or formatting is applied — rendering is kept minimal.
* MathJax 3 is used for cross-platform MathML support.

---

## 📬 Contact

**Developer:** Ankit Kumar
**Email:** [ankit.kumar@aus.ac.in](mailto:ankit.kumar@aus.ac.in)

---

🎯 This frontend was designed with cross-platform simplicity and full MathML compatibility in mind.
