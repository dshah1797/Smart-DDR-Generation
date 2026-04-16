# DDR Report Generator

## Overview
This project generates a **Detailed Diagnosis Report (DDR)** in **PDF format** from two input documents:

- **Thermal Images.pdf**
- **Sample Report.pdf**

The system extracts relevant observations, combines evidence from both reports, avoids duplicate points, handles missing or conflicting details, and produces a **client-friendly final DDR** similar in structure to the reference output format.

The generated report includes:

1. Property Issue Summary  
2. Area-wise Observations  
3. Probable Root Cause  
4. Severity Assessment with reasoning  
5. Recommended Actions  
6. Additional Notes  
7. Missing or Unclear Information  

It also extracts and places relevant images from the source PDFs in appropriate sections of the final report.

---

## Features
- Extracts text from inspection and thermal PDF reports
- Extracts page images from the source PDFs
- Links area-wise observations with supporting thermal evidence
- Avoids duplicate findings
- Handles missing data by explicitly marking **Not Available**
- Detects possible conflicts in evidence conservatively
- Generates:
  - **Final DDR PDF**
  - **Structured JSON output**
- Designed to generalize to similar inspection and thermal reports

---

## Input Files
Place these files in the same working directory before running the script:

- `Thermal Images.pdf`
- `Sample Report.pdf`

Optional reference file:
- `Main DDR.pdf`  
  This is only for style/reference understanding and is not required by the script logic.

---

## Output Files
The script creates an output folder:

```bash
ddr_output/
