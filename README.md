# 🩺 Oncology Treatment Monitoring Panel – Brazil (2013–2023)

## Dataset link :

## 📁 Description of Files and Folders

- **`data/CNV`**: CNV files. Contains the description of the encoded values of the dataset columns.
- **`docs/`**: Documents about the dataset avaliable in [DataSUS - File Transfer](https://datasus.saude.gov.br/transferencia-de-arquivos/).
- **`TAB415/`**: A version of Tabwin software.

- **`How to obtain data from DataSUS.ipynb`**: Steps on how the dataset [Oncology Treatment DataSUS – Brazil (2013–2023)](https://www.kaggle.com/datasets/lhucastenorio/oncology-treatment-datasus-brazil-20132023) was obtained



### Overview

This dataset contains anonymized records of cancer diagnosis and the initiation of oncological treatment in Brazil, carried out through the public health system (SUS – Sistema Único de Saúde) between 2013 and 2023. The data were compiled from the **Oncology Treatment Monitoring Panel (Painel-Oncologia)**, developed by Brazil’s Ministry of Health and processed by DATASUS.

The dataset is designed to monitor compliance with **Law No. 12.732/2012**, which mandates that patients diagnosed with malignant neoplasia begin treatment within 60 days of diagnosis.

---
### Dataset origin

It is worth noting that this dataset was uploaded as a `.csv` file. Due to this, it contains **only 20% of the original data** (which would be around 600 MB in `.csv` format). The full dataset is available on [DataSUS](https://datasus.saude.gov.br/transferencia-de-arquivos) as compressed database files (in `.dbc` format).

The steps for decompressing and processing the original database are detailed in the Jupyter Notebook titled [How to Obtain Data from DataSUS](https://github.com/tenoriolms/dataset_PO_DataSUS/blob/main/How%20to%20obtain%20data%20from%20DataSUS.ipynb). If you are interested in working more extensively with this dataset, it is recommended to use the complete data.

Nevertheless, the 20% sample provided here is sufficient to gain insights into Brazil’s public oncology treatment system.

---

### Data Sources

The records are derived from several SUS health information systems:

- **SIA-SUS**: Outpatient Information System  
- **SIH-SUS**: Hospital Information System  
- **SISCAN**: Cancer Information System  

These systems are integrated and consolidated by DATASUS, forming a unified database on cancer diagnoses, treatment modalities, and timing between diagnosis and treatment.

---

### Time Period

- Diagnosis data: from **2013 to 2023**  
- Treatment data: available starting in **2013**, with more complete records from **May 2018** onward, when the registration of CNS and ICD-10 codes became mandatory.

---

### Dataset Structure

Each row represents an oncological case identified by a unique National Health Card (CNS) and ICD-10 code. Main variables include:

| Column           | Description                                                                 |
|------------------|-----------------------------------------------------------------------------|
| `ano_diagn`      | Year of diagnosis (YYYY)                                                    |
| `ano_tratam`     | Year of first treatment (YYYY)                                              |
| `tempo_trat`     | Time interval between diagnosis and first treatment (in days)               |
| `tratamento`     | First treatment modality (surgery, chemo, radiotherapy, both, etc.)         |
| `diagnostic`     | Diagnostic category (malignant, in situ, uncertain behavior)                |
| `diag_deth`      | Detailed diagnosis code (ICD-10)                                             |
| `idade`          | Age at diagnosis                                                            |
| `sexo`           | Patient sex                                                                 |
| `estadiam`       | Cancer stage at treatment (I, II, III, IV, not applicable, unknown)         |
| `uf_resid`       | State of residence (IBGE code)                                              |
| `mun_resid`      | Municipality of residence (IBGE code)                                       |
| `uf_diagn`       | State where diagnosis occurred                                              |
| `mun_diag`       | Municipality where diagnosis occurred                                       |
| `uf_tratam`      | State where treatment was initiated                                         |
| `mun_tratam`     | Municipality where treatment was initiated                                  |
| `dt_diag`        | Date of diagnosis (DD/MM/YYYY)                                              |
| `dt_trat`        | Date of first treatment (DD/MM/YYYY)                                       |
| `dt_nasc`        | Patient’s date of birth (DD/MM/YYYY)                                        |

---

### Potential Uses

- Analyze treatment delays and time-to-treatment after cancer diagnosis.
- Map regional disparities in access to cancer care across Brazil.
- Study epidemiological patterns by sex, age, cancer type, and geography.
- Build predictive models to identify risk factors for delayed treatment.
- Support public health planning and cancer care policies.

---

### Important Notes

- The dataset includes only **SUS-registered patients with a valid National Health Card (CNS)**.
- Some variables may have missing data, especially before 2018.
- Negative intervals between diagnosis and treatment may occur in surgical cases where treatment preceded the formal diagnosis record.

---

### References

- Oncology Panel: http://tabnet.datasus.gov.br/cgi/painel_onco/  
- Technical Note (PDF): http://tabnet.datasus.gov.br/cgi/painel_onco/doc/painel_oncologia.pdf  
- Law No. 12.732/2012: http://www.planalto.gov.br/ccivil_03/_ato2011-2014/2012/lei/l12732.htm  


This dataset is based on public health records released by the Brazilian Ministry of Health. It is publicly available and can be used freely with proper attribution to the source.

