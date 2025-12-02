# FormGuard AI 🏥  
### Intelligent Pre-Validation for Healthcare Forms and Census Files  
**COT6930 – Generative Intelligence & SDLC**  
**Ali Arslan – Fall 2025**

---

## 📌 Project Overview  
FormGuard AI is a lightweight healthcare operations tool that pre-validates structured enrollment forms and census files **before** they enter downstream workflows.  
The goal is simple: **catch missing fields, invalid dates, formatting inconsistencies, and logic errors early**, reducing manual rework and improving data-quality throughput.

The solution uses a **single-agent LLM pipeline** (OpenAI GPT model) deployed in a Google Colab environment, paired with a **simulated web-based frontend** for demonstration purposes.

---

## 🚀 Features  
### ✔ LLM-powered form validation  
- Detects missing or invalid fields  
- Checks date consistency and logic (e.g., StartDate < EndDate)  
- Identifies malformed census rows  
- Suggests corrected output while keeping the original structure

### ✔ Human-in-the-loop workflow  
- Displays issues + corrected version side-by-side  
- User approves or makes edits manually  
- Download corrected file (in simulated UI)

### ✔ Simulated web UI prototype  
- Built with HTML/CSS/JS  
- Shows how the full product would look in a deployed future version  
- Mirrors the design and workflow of the actual backend  
- Purely frontend; no live API calls (safe for class submission)

### ✔ MVP Backend (Google Colab)  
- Reads `.csv` or `.txt` census files  
- Converts tabular data into structured text  
- Sends to LLM with strong prompt-engineering constraints  
- Outputs:
  - Error Summary  
  - Issues Detected  
  - Corrected Form  

---

## 🧠 System Architecture  
FormGuard AI follows a **simple three-layer architecture**:

1. **User Interaction Layer** (HTML prototype)  
   – Allows users to paste/upload census data  
   – Displays issues and corrected form  
   – Supports file downloads  

2. **Generative AI Processing Layer** (Colab notebook)  
   – Pre-processing  
   – LLM validation  
   – Error extraction  
   – Correction generation  

3. **Storage Layer** (local for demo)  
   – Synthetic census files  
   – Corrected outputs  

This design aligns with the course requirements of clarity, traceability, and human oversight.

---

## 🧪 Testing  
A set of synthetic census files were created to stress-test the system.  
Key metrics:

- **~90%** missing-field detection rate  
- **~85%** invalid-format detection  
- **0 hallucinated fields** after final prompt refinement  
- **4–6 seconds** per validation request  
- **High precision**—very few false positives  

Evaluation included both automated checks and manual review.

---

## ▶ How to Run the MVP Backend  
1. Open the Colab notebook inside: `backend/FormGuardAI_MVP.ipynb`  
2. Upload any `.csv` or `.txt` file to the notebook  
3. Run the validation cell  
4. View generated:
   - Summary  
   - Issues  
   - Corrected Form  
5. Download corrected output

No deployment required — runs entirely in Colab.

---

## ▶ How to Open the Frontend Simulation  
1. Navigate to: `frontend/FormGuardAI.html`  
2. Click **Raw** → **Save As…** to download  
3. Open the file in your browser  
4. Paste census data or upload  
5. Click **Run Validation** to trigger the simulated output  
6. Download corrected form (simulated)

---

## 🎯 Purpose & Vision  
FormGuard AI demonstrates how **Generative Intelligence** can remove repetitive overhead from healthcare operations by:

- Reducing manual form review  
- Catching errors earlier  
- Improving efficiency  
- Supporting a scalable workflow for payers and vendors  

This project aligns with real-world processes in enrollment ops and showcases an SDLC-driven GenAI design.

---

## 📩 Contact  
**Ali Arslan**  
Florida Atlantic University   

