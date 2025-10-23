# Invoice-Recognition-System-Using-Deep-Learning
# Automated Invoice Data Extraction: Advancements and Challenges in OCR-Based Approaches

**Summary**  
This project presents an **automated invoice recognition system (IRS)** that extracts structured data from invoices using **Optical Character Recognition (OCR)** and **Deep Learning** techniques.  
It replaces manual invoice entry by detecting, reading, and structuring invoice content efficiently, improving **accuracy**, **speed**, and **financial workflow automation**.

---

## **Project Overview**

The system processes scanned or digital invoices through a sequence of preprocessing, detection, recognition, and post-processing stages to extract key fields like invoice number, vendor name, date, and total amount.  
It is particularly designed for organizations handling large volumes of invoices.

---

## **Abstract**
Manual invoice processing is time-consuming and error-prone due to diverse formats and layouts.  
The proposed **Invoice Recognition System** utilizes OCR and deep learning to automate the process, standardize extraction, and deliver reliable digital output.  
This integration increases accuracy and supports business digitalization.

---

## **Workflow Diagram**

**Fig. 1: Flow Diagram of the Invoice Recognition System**

![Flow Diagram](images/flow_diagram.png)

This flow represents the stepwise process of preprocessing, text detection, OCR recognition, post-processing, and data validation.

---

## **OCR Illustration**

**Fig. 2: Introduction to OCR**

![OCR Overview](images/ocr_overview.png)

OCR (Optical Character Recognition) converts images of text into machine-readable text by analyzing shapes, fonts, and character patterns.

---

**Fig. 3: OCR in Invoice Recognition**

![OCR Process](images/ocr_in_invoice.png)

OCR is applied to scanned invoice documents to extract fields like vendor, invoice ID, amount, and date, minimizing manual data entry errors.

---

## **Objectives**
- Automate invoice data extraction using OCR and deep learning  
- Improve the speed and accuracy of financial document processing  
- Design a scalable and adaptable system for various invoice templates  
- Reduce human dependency in repetitive administrative work  

---

## **Methodology**

1. **Data Acquisition**  
   Collection of diverse invoice images with varying formats, orientations, and noise levels.

2. **Data Preprocessing**  
   - Scaling, normalization, denoising, and contrast enhancement  
   - Grayscale conversion and background artifact removal  
   - Color normalization for consistent OCR input

3. **Text Detection**  
   - Contour and bounding-box detection to localize text regions  
   - Use of frameworks like **EAST** or **YOLO** for robust scene-text localization

4. **Text Recognition (OCR)**  
   - Utilized **Tesseract OCR** engine with training and fine-tuning for invoice text  
   - Extracted multilingual data using adaptive language models

5. **Post-Processing**  
   - Applied regex-based validation for invoice number and date fields  
   - Spell and dictionary checks to correct text errors  
   - Confidence thresholding to filter unreliable outputs

6. **Feature Extraction**  
   Extracted structured attributes (invoice number, vendor name, date, total) and stored them in **JSON format** with bounding box coordinates.

7. **Validation and Integration**  
   Integrated validated data into financial workflows for automated entry and auditing.

---

## **Sample Input and Output**

**Fig. 4: Input Invoice**

![Input Invoice](images/input_invoice.png)

**Fig. 5: JSON Output Structure**

![JSON Output](images/json_output.png)

**Fig. 6: Bounding Box Visualization**

![Bounding Boxes](images/bounding_boxes.png)

---

## **Results and Discussion**
- Extracted text from invoice images using OCR with bounding-box localization  
- Converted recognized fields into structured JSON output  
- Achieved robust results even with varied invoice layouts  
- Continuous improvements through model tuning and error analysis

**Example JSON Snippet**
```json
{
  "Invoice_Number": "INV-00123",
  "Vendor_Name": "ABC Traders",
  "Invoice_Date": "2024-05-21",
  "Total_Amount": "₹45,800",
  "BoundingBox": [325, 240, 450, 265]
}
