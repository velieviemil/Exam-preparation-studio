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
<img width="795" height="377" alt="Screenshot 2026-11-14 161510" src="https://github.com/user-attachments/assets/3799985d-f0a9-4de5-95cb-6bb026a0280d" />
<img width="2558" height="1095" alt="Screenshot 2026-11-14 161456" src="https://github.com/user-attachments/assets/4d53a5ad-1ff3-44d8-b8d4-9a400f91d05b" />
<img width="2559" height="1347" alt="Screenshot 2026-11-14 161447" src="https://github.com/user-attachments/assets/c99b344c-6e6d-48d3-a284-02cf38b5e5ff" />

---

## 🛠️ Tech Stack

* **Core:** HTML5, Vanilla JavaScript (ES6+)
* **Styling:** [Tailwind CSS](https://tailwindcss.com/) (via CDN)
* **PDF Processing & Rendering:** [PDF.js](https://mozilla.github.io/pdf.js/) (`v3.11.174`)
* **Client-Side Storage:** `localStorage` (Quiz state, settings, history) & `IndexedDB` (Cropped equation/question images)
