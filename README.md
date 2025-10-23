# Invoice-Recognition-System-Using-Deep-Learning

This repository presents an **end-to-end implementation of the Invoice Recognition System (IRS)** .The project automates the extraction of key invoice information using **Optical Character Recognition (OCR)**, **Deep Learning**, and **AI-based text understanding**.  It was implemented and tested in **Google Colab**, and the final working model is **hosted on Gradio** for real-time interaction.

---

## Overview

Manual invoice processing is slow, repetitive, and error-prone due to varied invoice layouts and unstructured data formats. This project introduces a scalable system that reads invoice images, detects relevant regions, performs OCR, and generates a **structured JSON output**. The system minimizes manual intervention while improving **accuracy**, **speed**, and **data consistency** in financial workflows.The repository integrates both research insights and advanced AI modules for practical deployment.

---

## Key Highlights

- Fully executable **Google Colab notebook** with GPU support  
- Combines **traditional OCR concepts** (as detailed in the research) with **modern AI models** (SAM, DINO, Mistral)  
- Complete automation pipeline from preprocessing to field extraction  
- Interactive **Gradio interface** for user testing and live output visualization  
- Adaptable to multiple invoice templates and document formats  

---

## Research Foundation

The original study analyzed the potential of **Optical Character Recognition** and **Deep Learning** to automate financial document processing.  
The main goals included:
- Evaluating OCR’s accuracy for structured field recognition  
- Reducing human error and manual intervention  
- Handling variability in invoice designs  
- Improving data readiness for digital systems

This repository builds on that academic foundation and transforms it into a **functional prototype** with applied enhancements.

---

## Methodology

### 1. Data Acquisition
A diverse dataset of invoices (printed and scanned) was collected to represent multiple layouts, languages, and resolutions.

### 2. Image Preprocessing
Improves input quality for better OCR results.
- Scaling, normalization, denoising, and contrast enhancement  
- Grayscale conversion and artifact removal  
- Color normalization for consistent readability  

### 3. Text Region Detection
Implements **Grounding DINO** and **Segment Anything Model (SAM)** for object detection and segmentation of invoice areas.  
These help localize text-rich zones before OCR, improving recognition precision.

### 4. Optical Character Recognition (OCR)
Performed using **Tesseract OCR** to recognize characters and numbers from invoice regions.  
Extracted text includes invoice number, vendor name, date, and amount fields.

### 5. Post-Processing
- Regex validation for invoice number and date formats  
- Spell correction and confidence thresholding  
- Structured formatting for extracted entities  

### 6. LLM-Based Field Structuring
Cleaned text is processed through **Mistral 7B LLM** using **LangChain** and **Transformers**.  
The model identifies and structures extracted data into **JSON format**, ensuring consistent field labeling.

### 7. Output Visualization
- Bounding boxes drawn on invoice images for detected text regions  
- Extracted data displayed in structured JSON format  

### 8. Deployment via Gradio
The final Colab cell launches a **Gradio interface** allowing:
- Image/PDF upload  
- On-screen OCR visualization with bounding boxes  
- Real-time JSON data extraction  

---
## Bounding Box Visualization

The model visualizes detected text regions on the invoice image using bounding boxes.  
Each green box represents text successfully identified by the OCR engine, allowing visual verification of recognized data.  
This step helps validate segmentation accuracy and ensures that the extracted fields correspond correctly to their positions on the document.

---

## Gradio Live Demo

After successful execution in **Google Colab**, the notebook automatically launches a **Gradio web application**.  
Through this interface, users can:

- Upload invoice images or PDF files  
- View detected text regions with bounding boxes  
- Instantly see extracted text and structured JSON outputs in real time  

The Gradio app provides an intuitive and interactive environment to test the end-to-end model without needing to run code locally.

---

## Technologies and Libraries Used

- **Google Colab** – Primary execution environment  
- **Python 3.10+** – Core programming language  
- **OpenCV**, **NumPy**, **Pandas**, **Matplotlib**, **Seaborn** – Image processing and visualization  
- **Pytesseract** – Optical Character Recognition for text extraction  
- **Grounding DINO**, **Segment Anything (SAM)** – Deep learning models for layout and text region detection  
- **LangChain**, **Transformers**, **Mistral 7B** – For semantic understanding and structured JSON generation  
- **PyMuPDF**, **pdf2image** – Conversion of PDF invoices to image format  
- **Gradio** – Deployment framework for interactive web interface  

---

## Results and Discussion

- Achieved accurate extraction of invoice details from multi-format invoices using OCR  
- Improved localization and segmentation through **SAM** and **DINO** integration  
- Successfully structured extracted data into standardized **JSON format** for automation compatibility  
- Reduced manual effort and processing time compared to traditional invoice handling  
- Delivered an interactive **Gradio-based visualization**, enabling live validation of extraction results  

This practical implementation validates the findings of the original research while extending it through advanced AI and deep learning components.

---

## Limitations

- Performance depends on image clarity, lighting, and document alignment  
- Large model dependencies (SAM, DINO, Mistral) increase setup time in Google Colab  
- OCR accuracy decreases for handwritten or heavily blurred invoices  
- Requires **GPU runtime** for optimal speed and model performance  

---

## Future Scope

- Integration of **LayoutLMv3**, **Donut**, or similar end-to-end document understanding models  
- Expansion to **multi-language OCR support** for global invoice formats  
- Development of a **REST API or web-based microservice** for enterprise use  
- Optimization for real-time deployment with lightweight model alternatives  

---

## Achievements and Recognition

- Project successfully implemented and published in the  
  **International Journal of Scientific Research in Engineering and Management (IJSREM)**  

  **Title:** Automated Invoice Data Extraction: Advancements and Challenges in OCR-Based Approaches  
  **Volume:** 8, Issue 6 | June 2024  
  **ISSN:** 2582-3930 | **DOI:** [10.55041/IJSREM35494](https://doi.org/10.55041/IJSREM35494)

- Recognized for bridging **theoretical OCR-based research** with **real-world AI-driven automation**  
- Demonstrated the practical feasibility of using **OCR and LLMs** for enterprise-level data extraction  
- Integrated research insights into a functioning, scalable prototype hosted on Gradio for public testing  


