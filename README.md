# Finance News Named Entity Recognition (NER) Dataset

## Overview
This repository contains a custom-built dataset for Named Entity Recognition (NER) extracted from Indonesian financial news articles. The dataset is annotated with a comprehensive set of entity tags tailored to the economic and financial domain. Additionally, benchmarks have been conducted using state-of-the-art BERT models to evaluate the performance of this dataset.

## Named Entity Tag List
In general dataset includes these following entity tags, but in this project we use BIO-Format. So the tag below will be followed by at least the symbol B- as a marker for the start of the phrase:

- **DAT (Date):** Entities representing dates, such as "January 1, 2024" or "Q1 2023".
- **EVT (Event):** Entities representing specific events or occurrences.
- **GPE (Global Political Entity):** Entities representing geopolitical entities, such as countries, regions, or cities.
- **LOC (Location):** Entities representing specific physical locations, excluding political entities.
- **PER (Person):** Names of individuals or specific persons.
- **PRD (Product):** Entities representing products, such as devices, services, or brand names.
- **PRC (Percentage):** Entities representing percentages, such as "25%" or "4.5%".
- **CRD (Cardinal Number):** Cardinal numbers, such as quantities or counts.
- **TIM (Time):** Entities representing times, such as hours, minutes, or specific time periods.
- **NOR (Institution or Organization):** Nominal references to institutions or organizations, such as government institutions or community organizations.
- **ECONOMIC_INDICATOR:** Entities representing specific economic indicators, such as GDP, inflation, or interest rates.
- **ASSET_CLASS:** Entities representing specific categories of assets in the financial domain, such as stocks, bonds, or commodities.

## Benchmark Results
The dataset has been benchmarked using five BERT models. Below are the results:

| Model                               | Accuracy | F1 Score |
|-------------------------------------|---------|----------|
| **indobenchmark/indobert-base-p1**  |  0.97   | 0.76     |
| **indobenchmark/indobert-base-p2**  |  0.96   | 0.74     |
| **indobenchmark/indobert-large-p1** |  0.94   | 0.54     |
| **indolem/indobert-base-uncased**   |  0.96   | 0.70     |
| **LazarusNLP/NusaBERT-large**       |  0.96   | 0.71     |

*Note: Replace X.XX with actual benchmark values.*

## Dataset Creation Methodology
The dataset was constructed using a hybrid approach:

1. **Chunking Phrase:** Key phrases were identified and extracted using linguistic rules and chunking techniques.
2. **Term List Matching:** A curated list of domain-specific terms was utilized to identify and annotate entities.
3. **Model Assistance:** The pre-trained model `cahya/bert-base-indonesian-NER` was employed to assist in the annotation process, enhancing the accuracy and consistency of entity tagging.

## Usage
To use this dataset, clone this repository and load the dataset in your desired format (e.g., JSON, CSV, etc.). Ensure proper citation if using this dataset in your research.

```bash
# Clone the repository
git clone https://github.com/your-username/FinanceNewsNER.git

# Navigate to the directory
cd data/FinanceNewsNER.csv
```

## Future Work
- Expand the dataset to include more diverse financial news sources.
- Enhance the annotation process with additional domain-specific models.
- Perform further benchmarking with other NLP models.

## Citation
If you use this dataset in your work, please cite it as follows:

```
@dataset{Hilmi, Dkk._2024_FinanceNewsNER,
  author    = {Hilmi, Dkk.},
  title     = {Finance News Named Entity Recognition Dataset},
  year      = {2024},
  url       = {https://github.com/dhiiil/FinanceNewsNER}
}
```

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact
For any questions or feedback, please contact [fadhilahhilmi04@gmail.com].

