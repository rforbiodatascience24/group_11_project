# Data analysis on Gene Expression Analysis of Colorectal Cancer samples

## Project Contributors:

-   Group 11

    | Name                | Student ID | Github ID      |
    |---------------------|------------|----------------|
    | Eleni-Sofia Tseperi | s240066    | elenitsep      |
    | Johanne Lund        | s233246    | Yoyoyohanne    |
    | Marie Picquet       | s233736    | mariep00       |
    | Eglantine Anton     | s233242    | EglantineAnton |
    | Qiuyan Wu           | s241063    | s241063        |

## Data Retrieval:

The dataset for this project is taken from a dataset on Kaggle called Real Colorectal Cancer Datasets..

The data_url is <https://www.kaggle.com/api/v1/datasets/download/amandam1/colorectal-cancer-patients>.

## Dataset Information:

### Source

The datasets were obtained from the study *Gene Expression in Colorectal Cancer* conducted by Queen's University Belfast Cancer Research.

### Description

The data consists of a group of colorectal cancer patients, who underwent surgery to remove their tumors: one dataset contains patient data, and the other captures their respective gene expression level.

The dataset (Colorectal_Cancer_Patient_Data.csv) consists of the group of colorectal cancer patients data. It includes the following variables:

-   **ID_REF:** patient ID

-   **Age:** at Diagnosis (in Years)

-   **Dukes Stage:** A to D (development/progression of disease)

-   **Gender:** Male or Female

-   **Location:** Left, Right, Colon or Rectum

-   **DFS:** Disease-free survival, months (survival without the disease returning)

-   **DFS event:** 0 or 1 (with 1 = event)

-   **Adj_Radio:** If the patient also received radiotherapy

-   **Adj_Chem:** If the patient also received chemotherapy

The gene expression dataset (Colorectal_Cancer_Gene_Expression_Data.csv) contains gene expression levels for the same set of patients. This data has already been pre-processed and log2 transformed.

Link to the project presentation :

<https://github.com/rforbiodatascience24/group_11_project/blob/main/doc/presentation.html>,

## Run the Analysis

You can run the entire process in an R script: 00_all.qmd

R script path: \~/projects/group_11_project/R/00_all.qmd

## Project Structure

| Path        | Description                  |
|-------------|------------------------------|
| `data/_raw` | Raw input data               |
| `data/`     | Wrangled data files          |
| `doc/`      | Presentation                 |
| `R/`        | R scripts for analysis       |
| `results/`  | Output files (plots, tables) |
