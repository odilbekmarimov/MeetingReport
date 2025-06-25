# Star Schema Design and Implementation Task

## Objective

Design and implement a **Star Schema** using Python. The data provided in the Excel files (`raw_data.xlsx` and `final_data.xlsx`) represents meeting informations. Your task is to transform this data into a dimensional model suitable for analytical processing.

---

## Files Provided

- `raw_data.xlsx`: Contains raw transactional and dimensional data.
- `final_data.xlsx`: Represents a cleaned or consolidated version that may serve as a reference for output validation.

---

## Task Requirements

### 1. Understand the Data

- Load both Excel files using the `pandas` library.
- Explore the datasets to identify:
  - **Fact data**: Numeric/measurable values (e.g., sales amount, units sold).
  - **Dimension data**: Descriptive attributes (e.g., product name, customer region).

### 2. Define Star Schema Components

#### Fact Table

- Identify the central table that holds measurable values.
- Include appropriate foreign keys to reference each dimension table.

#### Dimension Tables

Create all the tables in the `final_data.xlsx`:



Ensure dimension tables:
- Contain unique records (deduplicated)
- Have clear primary keys
- Contain only relevant descriptive attributes

### 3. Build Schema in Python

- Use Python and `pandas` to:
  - Create clean dimension tables as separate DataFrames.
  - Build a fact table containing foreign key references to dimensions.
- Assign surrogate keys if necessary.

### 4. Export Tables

- Export each dimension and the fact table as separate sheets of same Excel file.


---

## Validation (Recommended)

- Verify that all foreign key relationships between the fact and dimension tables are intact.
- Optionally compare your final tables with `final_data.xlsx` for accuracy.

---

## Deliverables

1. Python script or Jupyter Notebook containing:
   - Data loading and preprocessing
   - Schema design logic
   - Dimension and fact table creation
   - Export commands

2. Output files: Excel file.

3. A visual diagram of your star schema using Power BI or any schema visualizer.

---

## Submission Deadline

Please submit all required deliverables by **Sunday, June 19, 21:00 **.
