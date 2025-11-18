# EXPIRY DATE RECOGNITION USING CNN & RESNET-50

A production-ready **Expiry Date Recognition System** that automatically detects, extracts, and validates expiry dates from product images using a hybrid pipeline of **CNN (ResNet-50)**, **OCR engines**, and **AI-based text analysis**.

The system is designed for **retail, pharma, and supply-chain** workflows where manual checking of expiry dates is slow and error-prone.

---

## 🎥 Project Demo

> Demo video is stored in the `WORKING DEMO VIDEO` folder of this repository.

```html
<!-- TODO: change YOUR_VIDEO_FILE_NAME.mp4 to the actual file name -->
<video src="https://github.com/ankush2992/7TH-SEM-MINOR-PROJECT/raw/main/WORKING%20DEMO%20VIDEO/YOUR_VIDEO_FILE_NAME.mp4"
       controls
       width="720">
  Your browser does not support the video tag.
</video>
```

👉 If the embedded player doesn't show in GitHub, users can still click this direct link:

[▶ Watch the demo](https://github.com/ankush2992/7TH-SEM-MINOR-PROJECT/raw/main/WORKING%20DEMO%20VIDEO/Video 2025-11-18 at 12.46.14_86147cf7.mp4)

---

## 🧾 Project Overview

The **Expiry Prediction System** automates the complete pipeline of expiry date detection:

1. **Image Input** – Users upload product/label images via a web interface.
2. **Preprocessing** – Images are cleaned (grayscale, denoising, contrast tweaks) to boost OCR performance.
3. **OCR & Text Extraction** – Text is extracted using **PaddleOCR** and **Azure Vision OCR**, handling low-quality prints and multiple languages.
4. **AI-Driven Date Understanding**
   - Local algorithms + **Regex** to detect common and rare date patterns
   - GPT / Gemini-style AI fallback when text is noisy or non-standard
5. **Expiry Status Calculation** – Extracted date is parsed, validated, and compared with today's date to label the product as **EXPIRED** or **NOT EXPIRED**.
6. **Web Output** – The website shows:
   - Original image
   - Annotated image / detection region
   - Detected expiry date + status
   - Additional product text / translations

---

## ✨ Key Features

- 📷 **Expiry Date Detection from Images**  
  Handles multiple fonts, noisy images, and real-world packaging variations.

- 🔍 **Hybrid OCR Pipeline**
  - **PaddleOCR** for fast local detection
  - **Azure Vision OCR** for robust cloud-based recognition and multi-language support

- 🧠 **AI + Regex-Based Date Parsing**  
  Smart logic to recognize formats like `DD/MM/YYYY`, `YYYY-MM-DD`, compact numeric forms, and unusual patterns.

- 🌐 **Web Interface**  
  Frontend built to let users upload images and instantly view predictions, translated text, and expiry status.

- ☁️ **Cloud Deployment (Azure VPS)**  
  Deployed with **Nginx + Gunicorn** on an Azure virtual machine, with domain & HTTPS support for production-style hosting.

- 🔒 **Security & Standards**  
  Designed with attention to secure API keys, HTTPS access, and software standards such as **PEP 8**, **IEEE**, and **ISO 25010/9126**.

---

## 🧱 System Architecture (High-Level)

- **Frontend**
  - HTML, CSS, JavaScript-based UI
  - Responsive layout for easy image upload and result visualization

- **Backend**
  - Python web server (Flask/FastAPI style)
  - Routes for:
    - Receiving image uploads
    - Running OCR modules
    - Running AI / regex date extraction
    - Returning expiry status + details as JSON/HTML

- **ML / AI Components**
  - CNN with **ResNet-50** backbone for date-region understanding and prediction
  - Local regex and rules for fast parsing
  - GPT/Gemini-style AI integration for complex cases

- **External Services**
  - **Azure Vision OCR** for robust text extraction
  - **Azure Translator** for translating non-English text into English

---

## 🛠 Tech Stack

- **Languages:** Python, JavaScript
- **DL / ML:** CNN, ResNet-50, PyTorch / similar frameworks
- **OCR:** PaddleOCR, Azure Computer Vision (OCR)
- **NLP / AI:** GPT-style models, regex-based parsing
- **Web:** Flask/FastAPI backend, HTML/CSS/JS frontend
- **Cloud & DevOps:** Azure VPS, Nginx, Gunicorn, HTTPS, basic CI/CD hooks

---

## 👥 Project Team

B.Tech CSE, 7th Semester – Minor Project, KIIT Deemed to be University

- **Samridhi Sinha** – *22051100*
- **Aastha Singh** – *22051653*
- **Umme Saleh** – *22051733*
- **Ankush Kumar** – *22051748*
- **Gaurav Kumar** – *22052206*

---

## 🎓 Guide

**Dr. Sourabh Debnath**  
School of Computer Engineering, KIIT Deemed to be University

---

## 📌 Note

This repository is primarily intended as a **project showcase** for academic evaluation and portfolio use.  
Runtime setup instructions, environment configuration, and deployment scripts are intentionally omitted here.
