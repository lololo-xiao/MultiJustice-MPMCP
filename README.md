# MultiJustice: A Chinese Dataset for Multi-Party, Multi-Charge Legal Prediction

[![Paper](https://img.shields.io/badge/Paper-NLPCC%202025-blue)](https://arxiv.org/abs/2507.06909)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

## Overview

**MultiJustice** introduces the MPMCP (Multi-Person Multi-Charge Prediction) dataset — **20,000 Chinese criminal cases** across four legal judgment scenarios that systematically vary in complexity:

| Scenario | Defendants | Charges | Cases |
|----------|-----------|---------|-------|
| **S1** | Single | Single | 5,000 |
| **S2** | Single | Multiple | 5,000 |
| **S3** | Multiple | Single | 5,000 |
| **S4** | Multiple | Multiple | 5,000 |

We benchmark five models (MT5, BERT, RoBERTa, Lawformer, InternLM2) on two tasks: **charge prediction** and **penalty term prediction**.

**Key finding**: S4 poses the greatest challenge. InternLM2 drops ~4.5% F1 from S1 to S4, while Lawformer drops ~19.7%.

## Results

### Charge Prediction (F1-Score %)

| Scenario | MT5 | BERT | RoBERTa | Lawformer | InternLM2 |
|----------|-----|------|---------|-----------|-----------|
| S1 | 76.4 | 78.6 | 81.0 | 81.4 | **85.3** |
| S2 | 72.0 | 66.3 | 70.5 | 72.4 | **91.8** |
| S3 | 70.9 | 77.8 | 75.2 | 78.0 | **81.0** |
| S4 | 64.3 | 60.1 | 62.1 | 61.7 | **80.8** |

### Penalty Term Prediction (LogD % — lower is better)

| Scenario | MT5 | BERT | RoBERTa | Lawformer | InternLM2 |
|----------|-----|------|---------|-----------|-----------|
| S1 | 60.7 | 45.8 | 43.3 | **39.5** | 59.3 |
| S2 | 62.0 | 51.5 | 49.3 | **46.4** | 54.1 |
| S3 | 79.8 | 53.6 | 51.7 | **48.7** | 61.3 |
| S4 | 68.3 | **56.8** | 57.1 | 58.5 | 56.5 |

## Data Format

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

## Citation

```bibtex
@inproceedings{wang2025multijustice,
  title={MultiJustice: A Chinese Dataset for Multi-Party, Multi-Charge Legal Prediction},
  author={Wang, Xiao and Pei, Jiahuan and Shui, Diancheng and Han, Zhiguang and Sun, Xin and Zhu, Dawei and Shen, Xiaoyu},
  booktitle={Proceedings of NLPCC 2025},
  year={2025}
}
```

## Contact

For questions about the dataset or code, please contact:
- Email: wangxiao02131@gmail.com

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
