# Data analysis on gene Expression Analysis of Colorectal Cancer samples

## Project Contributors:

-   Group 11

    -   Eleni-Sofia Tseperi (s240066) - elenitsep,

    -   Johanne Lund (s233246) - Yoyoyohanne,

    -   Marie Picquet (s233736) - mariep00,

    -   Eglantine Anton (s233242) - EglantineAnton,

    -   Qiuyan Wu (s241063) - s241063.

## Data Retrieval:

The dataset for this project is taken from the Gene Expression Omnibus (GEO) under the accession number [GSE50760](https://www.ncbi.nlm.nih.gov/geo/download/?acc=GSE50760 "data download").

In the below above, click on "Download RNA-seq counts".

Under NCBI-generated data, download the FPKM normalized data (GSE50760_norm_counts_FPKM_GRCh38.p13_NCBI.tsv.gz) and the Human gene annotation table (Human.GRCh38.p13.annot.tsv.gz)

## Dataset Information:

### Source

The dataset was obtained from the study *Gene Expression Profiling by RNA-seq in Colorectal Cancer* ([GSE50760](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE50760)), which aimed to identify a prognostic signature in colorectal cancer (CRC) patients, addressing the diverse progression and heterogeneity of CRCs.

### Description

This RNA-seq dataset comprises 54 samples from 18 colorectal cancer patients. The samples are distributed across three conditions:

-   Normal colon tissue

-   Primary colorectal cancer (CRC) tissue

-   Liver metastases

### Data Generation

-   **RNA Isolation**: Total RNA was extracted using the RNeasy Mini Kit (Qiagen, CA, USA), with quality confirmed via agarose gel electrophoresis and ethidium bromide staining, followed by visual examination under ultraviolet light.

-   **Library Preparation**: mRNA was purified, fragmented, converted to cDNA, and amplified using the TruSeq RNA Sample Preparation Kit v2 (Illumina).

-   **Sequencing**: Paired-end reads (2x100 bp) were generated using the Illumina HiSeq-2000 platform.

# TO DO

Make the data tidy and clean (flipping, joining, changing ID_ref etc...)

-   expr_data

    -   filp the table (ID_REF becomes the name of the columns, )

-   patient data

    -   take care of missing value

    -   add parameters (ex: BMI, etc.. -\> find stuff that can be calculated with the information we have)

    -   make age into age group

    -   turning gender to binary

    -   change month into years

-   join the table

-   delete all the columns we will not use

Data exploration

-   "Take a look at the data", make some plot

    -   numerical -\> table, mean value etc...

    -   categorical -\> bar charts (how many patients per category)
    
#########################
- Update describe if we change the dataset (Example if we delete columns)
- [extra] see if we can find a correlation between probe name (0000_at) and gene_id. Otherwise manually find gene_id for the few genes that we decide to analyze further and mutate a new column with only those (And the rest will be missing values).
