### Planning Document: Workflow for User-Guided Sorting in Word and Export to Excel

---

#### **Objective**
Enable users to extract text from a PDF, organize the data manually in Word by highlighting and applying labels with a single click, and then export the labeled content to an Excel file with columns for `Finnish Term`, `Swedish Term`, and `Description`.

---

### **Workflow Overview**

1. **PDF Extraction**
   - Extract text from a PDF file (e.g., glossary terms) into a structured Word document.
   - Separate Finnish terms, Swedish terms, and descriptions into individual sections for clarity.

2. **User-Guided Labeling in Word**
   - Provide a Word file with pre-defined styles for labeling text (e.g., *Finnish Term*, *Swedish Term*, *Description*).
   - Users can highlight text and apply the appropriate style using Word's ribbon or shortcuts.

3. **Process the Labeled Word File**
   - Use Python to read the styled content from the Word file.
   - Identify labeled text based on styles and organize it into categories.

4. **Export to Excel**
   - Map the labeled text to an Excel spreadsheet with columns for `Finnish Term`, `Swedish Term`, and `Description`.
   - Save the final Excel file for further use or sharing.

---

### **Detailed Steps**

#### **Step 1: PDF Extraction**
**Goal**: Extract terms and organize them into a Word file.

- **Input**: PDF file (e.g., `VNK_2023_17.pdf`).
- **Process**:
  - Extract text using `fitz` (PyMuPDF).
  - Structure the text into sections with placeholders for Finnish, Swedish, and descriptions.
  - Output a Word file.
- **Output**: A Word document with placeholders for the extracted text.

#### **Step 2: Prepare the Word Document for Labeling**
**Goal**: Enable user-friendly labeling in Word.

- **Define Styles**:
  - Create a Word template with predefined styles (`Finnish Term`, `Swedish Term`, `Description`).
  - Include clear instructions at the top of the document for users.

- **User Task**:
  - Highlight text in the Word file and apply styles using the Word ribbon or shortcuts.
  - Save the edited Word file.

#### **Step 3: Process Labeled Word File**
**Goal**: Extract labeled text from the edited Word document.

- **Input**: User-edited Word file.
- **Process**:
  - Use Python (`python-docx`) to identify text and its corresponding styles.
  - Map each styled paragraph to its category (`Finnish Term`, `Swedish Term`, `Description`).

#### **Step 4: Export to Excel**
**Goal**: Organize labeled text into an Excel spreadsheet.

- **Input**: Parsed labeled data.
- **Process**:
  - Use `openpyxl` to create an Excel file.
  - Map categories (`Finnish Term`, `Swedish Term`, `Description`) to separate columns.
- **Output**: An Excel file with structured content.

---

### **Deliverables**

1. **Python Scripts**
   - Script to extract PDF text and generate a Word file.
   - Script to process labeled Word file and export to Excel.

2. **Word Template**
   - A Word file with pre-defined styles for labeling (`Finnish Term`, `Swedish Term`, `Description`).

3. **Excel File**
   - Final Excel output with sorted columns.

---

### **Timeline**

| **Task**                              | **Estimated Working Time** | **Notes**                                      |
|---------------------------------------|--------------------|-----------------------------------------------|
| PDF Extraction Script                 | 1-2 days           | Ensure robust extraction for glossary format. |
| Word Template Creation                | 1 day              | Define styles and add usage instructions.     |
| Word Processing Script                | 2-3 days           | Handle style detection and data parsing.      |
| Excel Export Script                   | 1-2 days           | Map data to columns and handle formatting.    |
| Testing and Refinement                | 2-3 days           | User feedback and edge-case handling.         |

---

### **Tools and Libraries**

- **Text Extraction**: PyMuPDF (`fitz`).
- **Word File Processing**: `python-docx`.
- **Excel Export**: `openpyxl`.

---

Would you like me to create the Word template or the Python script for any specific step first?
```

You can copy and paste this formatted Markdown content into a new `.md` file in your repository to make it look nice on GitHub.
