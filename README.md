# FHIR Medications – Queries, Analysis, and Exploration

This repository accompanies a lesson on **FHIR medication resources** and demonstrates how to query, retrieve, and analyze medication-related data using FHIR R4, Python, and supporting tools.

It is intended for learners who are:

* New to FHIR medication resources
* Learning how to write FHIR REST queries
* Working with FHIR Bundles in Python
* Transitioning from raw JSON traversal to more structured approaches (FHIR models, FHIRPath)

---

## Repository Contents

### 📓 `medications.ipynb`

A Jupyter notebook that demonstrates:

* Executing FHIR REST searches for medication-related resources
* Parsing FHIR Bundle responses
* Extracting fields from resources such as `MedicationRequest` and `MedicationStatement`
* Working with FHIR data using **plain Python dictionaries** (JSON traversal)
* Preparing tabular outputs suitable for analysis or display

This notebook is designed to reinforce how FHIR resources are structured and how medication data is represented in real responses.

---

### 🌐 `search.http`

An HTTP file containing example **FHIR REST API queries**, suitable for use with:

* VS Code REST Client
* Postman (with minor adaptation)

The queries illustrate common medication-related patterns, including:

* Retrieving active prescriptions (`MedicationRequest`)
* Querying medication history (`MedicationStatement`)
* Filtering by patient, status, and date ranges
* Using standard FHIR search parameters

These queries align directly with the scenarios discussed in the slide deck.

---

### 📊 `FHIR Resources - Medications.pptx`

Lecture slides titled **“Understanding FHIR Medications – Exploring FHIR’s Approach to Medication Management.”**

Topics covered include:

* Roles and differences between:

  * `MedicationRequest`
  * `MedicationStatement`
  * `MedicationAdministration`
  * `Medication`
* Common clinical scenarios and correct resource selection
* Writing robust FHIR queries for medication data
* RxNorm and its role in medication interoperability
* Query patterns you will reuse frequently in real-world systems

These slides provide the conceptual foundation for the notebook and query examples.

---

### 📦 `requirements.txt`

Python dependencies required to run the notebook:

* **requests** – for HTTP calls to FHIR servers
* **fhir.resources** – strongly typed FHIR R4 resource models
* **fhirpathpy** – optional FHIRPath expression evaluation
* **pandas** – tabular data handling
* **matplotlib** – basic visualization support (used in later lessons)
* **ipykernel / notebook** – Jupyter support

Install dependencies with:

```bash
pip install -r requirements.txt
```

---

## Learning Objectives

By working through the materials in this repository, you will be able to:

* Choose the correct FHIR medication resource for common clinical scenarios
* Write effective FHIR search queries for medication data
* Understand how RxNorm is used in FHIR medication coding
* Parse and extract data from FHIR Bundles in Python
* Recognize the difference between:

  * Procedural JSON traversal in Python
  * Declarative FHIRPath expressions

---

## Prerequisites

* Basic familiarity with REST APIs
* Introductory knowledge of FHIR resources
* Python fundamentals
* Jupyter Notebook or VS Code environment

---

## Notes for Learners

* The Python examples intentionally use **raw dictionary access** to make FHIR JSON structure explicit.
* Later lessons may refactor these examples to use:

  * `fhir.resources` models
  * FHIRPath expressions
  * Database-backed analytics workflows

Understanding the underlying JSON first will make those transitions much easier.

---

## License / Usage

This repository is intended for **educational and training purposes**. Adapt and reuse examples as needed for learning, demos, and internal prototypes.

---

*Prepared as part of a FHIR application development curriculum focusing on practical, interoperable medication workflows.*
