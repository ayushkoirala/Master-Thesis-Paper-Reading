# Master-Thesis-Paper-Reading
I intend to write down everything I read during my studies.

-Paper on ParaPhrase Generation


#  Experiment

Masking Ratio (0.15)
| Masking Technique | Rouge1 | Rouge2 | RougeL | BERTScore |
|-------------------|--------|--------|--------|-----------|
| Random            |        |        |        |           |
| TF-IDF            |        |        |        |           |
| PICO              |        |        |        |           |

Masking Ratio (0.30)
| Masking Technique | Rouge1 | Rouge2 | RougeL | BERTScore |
|-------------------|--------|--------|--------|-----------|
| Random            |        |        |        |           |
| TF-IDF            |        |        |        |           |
| PICO              |        |        |        |           |

Masking Ratio (0.45)
| Masking Technique | Rouge1 | Rouge2 | RougeL | BERTScore |
|-------------------|--------|--------|--------|-----------|
| Random            |        |        |        |           |
| TF-IDF            |        |        |        |           |
| PICO              |        |        |        |           |


# Ablation Study: 1

| Generator | Rouge1 | Rouge2 | RougeL | BERTScore |
|-----------|--------|--------|--------|-----------|
| BARTbase  |        |        |        |           |
| BartLarge |        |        |        |           |
| BartCNN   |        |        |        |           |
| BartXsum  |        |        |        |           |

# Ablation Study: 2

| Generator                             | Rouge1 | Rouge2 | RougeL | BERTScore |
|---------------------------------------|--------|--------|--------|-----------|
| Top-k-sentences                       |        |        |        |           |
| Sum_len+Top-k-sentences               |        |        |        |           |
| Background+Top-k-sentences            |        |        |        |           |
| Sum_len+Background+Top-k-sentences    |        |        |        |           |


# Dataset Statistics

| Statistic                                        | Training Data              | Validation Data            |
|--------------------------------------------------|----------------------------|----------------------------|
| Number of rows missing Background                | 210                        | 38                         |
| Number of rows missing Target                    | 42                         | 0                          |
| Total number of unique ReviewID before dropping  | 14,188                     | 2,021                      |
| Total number of unique ReviewID after dropping   | 13,978                     | 1,983                      |
| Total number of unique ReviewID dropped          | 210                        | 38                         |
| Average number of tokens in Background per ReviewID | 73.46                    | 69.85                      |
| Average number of tokens in Target per ReviewID  | 61.26                      | 60.89                      |
| Average number of tokens in Abstract per ReviewID| 301.55                     | 299.97                     |



