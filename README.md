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


