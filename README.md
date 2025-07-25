# MultiJustice: A Chinese Dataset for Multi-Party, Multi-Charge Legal Prediction

[![Paper](https://img.shields.io/badge/Paper-NLPCC%202025-blue)](https://arxiv.org/abs/2507.06909)
[![Dataset](https://img.shields.io/badge/Dataset-HuggingFace-yellow)](https://huggingface.co/loss4Wang)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

## 📖 Overview

**MultiJustice** is a comprehensive Chinese legal dataset designed for multi-party, multi-charge legal judgment prediction (LJP). This dataset addresses the critical research question: *Should multiple defendants and charges be treated separately in LJP?*

Our dataset contains **20,000 Chinese legal cases** across four practical legal judgment scenarios, enabling researchers to evaluate the complexity of real-world legal prediction tasks.

## 🎯 Key Features

- **20,000** Chinese legal cases with case facts, charges, and penalty terms
- **4 Legal Scenarios** covering different complexity levels
- **2 Prediction Tasks**: Charge prediction and penalty term prediction
- **Comprehensive Evaluation** across multiple legal LLMs
- **Standardized Splits** for reproducible research

## 🏗️ Legal Scenarios

### Scenario 1 (S1): Single Defendant, Single Charge
The simplest case involving one defendant and one charge.

### Scenario 2 (S2): Single Defendant, Multiple Charges  
Cases where one defendant faces multiple charges simultaneously.

### Scenario 3 (S3): Multiple Defendants, Single Charge
Cases involving multiple defendants charged with the same offense.

### Scenario 4 (S4): Multiple Defendants, Multiple Charges
The most complex scenario with multiple defendants facing various charges.


**Key Finding**: Scenario S4 (multiple defendants, multiple charges) poses the greatest challenges, with performance degradation varying significantly across models.



## 🔧 Data Format

The dataset is provided in CSV format with the following columns:

| Column | Description |
|--------|-------------|
| `index` | Unique case identifier |
| `date` | Date of the verdict |
| `verdict` | Court verdict decision |
| `defendant` | Defendant name(s) |
| `accusation` | Legal accusation/charge |
| `relevant_law` | Applicable law reference |
| `province` | Province where case was tried |
| `defendant_accusation` | Specific accusations against defendant(s) |
| `fact` | Case facts in Chinese |
| `defendant_judgement` | Judgment for each defendant |
| `relevant_article` | Specific legal article references |
| `imprisonment` | Imprisonment duration (months) |
| `fact_len` | Length of fact text |





## 📧 Contact

For questions about the dataset or code, please contact:
- Email: wangxiao02131@gmail.com

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🔄 Updates

- **2025-07**: Initial release with 20,000 cases


