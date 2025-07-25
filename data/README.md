# MultiJustice Dataset Files

## Dataset Overview
This directory contains 20,000 Chinese legal cases split across 12 CSV files for multi-scenarioy, multi-charge legal judgment prediction.

## File Structure
- **Training Data**: 16,000 cases across 4 files (4,000 cases each)
  - `train_data1.csv` - Training set scenario 1
  - `train_data2.csv` - Training set scenario 2  
  - `train_data3.csv` - Training set scenario 3
  - `train_data4.csv` - Training set scenario 4

- **Test Data**: 2,000 cases across 4 files (500 cases each)
  - `test_data1.csv` - Test set scenario 1
  - `test_data2.csv` - Test set scenario 2
  - `test_data3.csv` - Test set scenario 3
  - `test_data4.csv` - Test set scenario 4

- **Validation Data**: 2,000 cases across 4 files (500 cases each)
  - `val_data1.csv` - Validation set scenario 1
  - `val_data2.csv` - Validation set scenario 2
  - `val_data3.csv` - Validation set scenario 3
  - `val_data4.csv` - Validation set scenario 4

## Data Format
Each CSV file contains the following columns:
- `index`: Unique case identifier
- `date`: Date of the verdict
- `verdict`: Court verdict decision
- `defendant`: Defendant name(s)
- `accusation`: Legal accusation/charge
- `relevant_law`: Applicable law reference
- `province`: Province where case was tried
- `defendant_accusation`: Specific accusations against defendant(s)
- `fact`: Case facts in Chinese
- `defendant_judgement`: Judgment for each defendant
- `relevant_article`: Specific legal article references
- `imprisonment`: Imprisonment duration (months)
- `fact_len`: Length of fact text