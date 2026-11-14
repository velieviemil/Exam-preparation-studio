# 🎓 ExamPrep Studio
You can use the site via the web using this link: https://velieviemil.github.io/Exam-preparation-studio/
**ExamPrep Studio** is a zero-backend, single-file web application designed to transform raw exam PDFs into an interactive, customizable quiz and revision platform. Built entirely with client-side technologies, it runs directly in the browser without requiring any server setup, database configuration, or internet connection after loading.

---

## ✨ Key Features

* **📄 Intelligent PDF Parsing Engine:** Automatically scans and extracts multiple-choice questions and answers from PDF documents using visual line grouping (Y-bucketing) and state-machine parsing.
* **🔢 Smart Marker Detection:** Recognizes standard bullet points (`•`, `-`, `*`) for options and checkmarks (`√`, `✓`, `✔`, etc.) for correct answers, while ignoring stray formatting noise.
* **🧮 Automatic Equation & Image Capture:** Detects math formulas, diagrams, or non-extractable text objects in questions and options, rendering those specific regions directly from the PDF page as clean, cropped images (while hiding the answer markers so they don't give away the solution).
* **⚙️ Customizable Exam Setup:** Allows users to select specific question ranges (e.g., Q1–100) and automatically generates a randomized **50-question** mock exam using the Fisher-Yates shuffle algorithm.
* **💾 Offline Persistence (LocalStorage & IndexedDB):** 
  * Automatically saves in-progress quiz drafts so you can resume anytime.
  * Stores extracted equation images locally in **IndexedDB** to bypass `localStorage` size limits.
  * Keeps a complete history of past exam attempts, scores, and completion times.
* **📊 Detailed Post-Exam Review:** Sorts results to prioritize **incorrect answers first**, displaying your selected answer alongside the correct solution (including cropped images for math questions).
* **🌓 Dark & Light Mode:** Clean, responsive UI built with Tailwind CSS featuring a persistent theme toggle.

---

## 🛠️ Tech Stack

* **Core:** HTML5, Vanilla JavaScript (ES6+)
* **Styling:** [Tailwind CSS](https://tailwindcss.com/) (via CDN)
* **PDF Processing & Rendering:** [PDF.js](https://mozilla.github.io/pdf.js/) (`v3.11.174`)
* **Client-Side Storage:** `localStorage` (Quiz state, settings, history) & `IndexedDB` (Cropped equation/question images)
