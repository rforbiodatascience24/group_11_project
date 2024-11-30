# Data analysis on gene Expression Analysis of Colorectal Cancer samples

## Project Contributors:

-   Group 11

    -   Eleni-Sofia Tseperi (s240066) - elenitsep,

    -   Johanne Lund (s233246) - Yoyoyohanne,

    -   Marie Picquet (s233736) - mariep00,

    -   Eglantine Anton (s233242) - EglantineAnton,

    -   Qiuyan Wu (s241063) - s241063.

## Data Retrieval:

The dataset for this project is taken from a dataset on Kaggle called Real Colorectal Cancer Datasets..

The data_url is <https://www.kaggle.com/api/v1/datasets/download/amandam1/colorectal-cancer-patients>.

Download data ,uzip and remove the zip file.

Use the "read_csv" to load data into matrix.

expr_file \<- "Colorectal_Cancer_Gene_Expression_Data.csv"

patient_file \<-"Colorectal_Cancer_Patient_Data.csv"

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

# TO DO

### **On the 01_load.qmd**

#### Make the data messy and dirty

The data set we are using is pretty clean and tidy. To increase the complexity of the project and use the skills we've acquired throughout the course, we decided to artificially introduce some dirtiness and messiness to the data, so that we can demonstrate our ability to handle raw data. In a real-world bio data science project, this step would, of course, be unnecessary.

For the expression data set:

-   We introduced 2% missing values in the gene expression level coded as N/A

-   We added "gene\_" at the beginning of all the gene names

For the patient data set:

-   We remplace 10% of "Male" by "M", and 10% of "Female" by "F"

-   We merged 3 variables together

-   We change the age of one patient to -2

-   We mix years and months in the DFS variable

#### Make the data tidy and clean (flipping, joining, changing ID_ref etc...)

-   expr_data

    -   filp the table (`ID_REF` becomes the name of the columns, )

-   patient data

    -   We need to split the column `DFS event/Adj_Radio/Adj_Chem` into 3 distinct variables.

    -   Convert everything in month to have one value per observation.

    -   The column `...1` doesn't represent any meaningful variable, so drop it.

-   Combine the two data sets by `ID_REF` ,pass the new dataset to `01_dat_load.tsv`

### **On the 02_clean.qmd**

Loading the `01_dat_load.tsv`

-   Cleaning row values

    The rows that don't correspond to a patient (i. e. don't have a valid ID_REF that starts with GSM) can be dropped.

    The genders are currently denoted as Male or M and Female or F, we convert everything into 0 for male and 1 for female.

-   Cleaning column names

    Modify the name of the columns to make them easier to work with later during the project

    -   The variables that have several words in their name are shorten into one word

        -   `Age (in years)` becomes `Age`

        -   `DFS (in months)` becomes `DFS`

        -   `Dukes Stage` becomes `Dukes_stage`

        -   `DFS event` becomes `DFS_event`

    -   `\_gene` is removed at the beginning of all the genes names to make them shorter

-   Pass the new dataset to `02_dat_clean.tsv`

### **On the 03_augment.qmd**

-   Creating new variables:

    -   `Age_group`:cut by 10

    -   `No_stage`:

        -   Dukes_stage "A",No_stage = 1.

        -   Dukes_stage "B",No_stage = 2.

        -   Dukes_stage "C",No_stage = 3.

        -   Dukes_stage "D",No_stage = 4.

    -   `metastasis`

    -   No_stage \<= 3 \~ 0, metastasis = 0.

    -   No_stage \> 3 \~ 1, metastasis = 1.

-   Pass the new dataset to `03_dat_aug.tsv`

Data exploration

-   "Take a look at the data", make some plot

    -   numerical -\> table, mean value etc...

    -   categorical -\> bar charts (how many patients per category)

######################### 

-   Update describe if we change the dataset (Example if we delete columns)
-   [extra] see if we can find a correlation between probe name (0000_at) and gene_id. Otherwise manually find gene_id for the few genes that we decide to analyze further and mutate a new column with only those (And the rest will be missing values).
