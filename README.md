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

The dataset was obtained from the study *Gene Expression in Colorectal Cancer* . These two datasets consists of a group of colorectal cancer patients, who had surgery to remove their tumour. One dataset on patient data and one of their respective gene expression levels.

### Description

This dataset (Colorectal_Cancer_Patient_Data.csv) consists of the group of colorectal cancer patients data.

The patient dataset consists of the following variables:

-   **Age:** at Diagnosis (in Years)

-   **Dukes Stage:** A to D (development/progression of disease)

-   **Gender:** Male or Female

-   **Location:** Left, Right, Colon or Rectum

-   **DFS:** Disease-free survival, months (survival without the disease returning)

-   **DFS event:** 0 or 1 (with 1 = event)

-   **Adj_Radio:** If the patient also received radiotherapy

-   **Adj_Chem:** If the patient also received chemotherapy

The gene expression dataset (Colorectal_Cancer_Gene_Expression_Data.csv) comprises of gene expression levels for the same set of patients.

This data has been pre-processed and log2 transformed. You need not make any further transformations to the data.

## Presentation

Link to the project presentation :

<https://github.com/rforbiodatascience24/group_11_project/blob/main/doc/presentation.html>,

## Run Analysis

You can run the whole process in R script : \~/projects/group_11_project/R/99_proj_func.R

## Project Structure

| Path       | Description                  |
|------------|------------------------------|
| `data/_raw`| Raw input data               |
| `data/`    | Wrangled data files          |
| `doc/`     | Presentation                 |
| `R/`       | R scripts for analysis       |
| `results/` | Output files (plots, tables) |
