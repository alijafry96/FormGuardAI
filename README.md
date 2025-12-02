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

## 📂 Repository Structure  

