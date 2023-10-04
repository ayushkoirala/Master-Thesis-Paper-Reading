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


# New Table:

# Masking Ratio (0.15) - PICO

| Model     | Input Variant                     | Metrics                                                                     |
|-----------|-----------------------------------|--------|--------|--------|-----------|--------|--------|--------|-----------|
|           |                                   | Validation Sample                    |Testing Sample                        |
|-----------|-----------------------------------|--------|--------|--------|-----------|--------|--------|--------|-----------|
|           |                                   | Rouge1 | Rouge2 | RougeL | BERTScore |Rouge1 | Rouge2 | RougeL | BERTScore  |
|-----------|-----------------------------------|--------|--------|--------|-----------|--------|--------|--------|-----------|
| BARTbase  | Background+Top-k-sentences        |        |        |        |           |        |        |        |           |
|           | Top-k-sentences                   |        |        |        |           |        |        |        |           |
|           | Sum_len+Top-k-sentences           |        |        |        |           |        |        |        |           |
|           | Sum_len+Background+Top-k-sentences|        |        |        |           |        |        |        |           |
|-----------|-----------------------------------|--------|--------|--------|-----------|--------|--------|--------|-----------|
| BartLarge | Background+Top-k-sentences        |        |        |        |           |        |        |        |           |
|           | Top-k-sentences                   |        |        |        |           |        |        |        |           |
|           | Sum_len+Top-k-sentences           |        |        |        |           |        |        |        |           |
|           | Sum_len+Background+Top-k-sentences|        |        |        |           |        |        |        |           |
|-----------|-----------------------------------|--------|--------|--------|-----------|--------|--------|--------|-----------|
| BartCNN   | Background+Top-k-sentences        |        |        |        |           |        |        |        |           |
|           | Top-k-sentences                   |        |        |        |           |        |        |        |           |
|           | Sum_len+Top-k-sentences           |        |        |        |           |        |        |        |           |
|           | Sum_len+Background+Top-k-sentences|        |        |        |           |        |        |        |           |
|-----------|-----------------------------------|--------|--------|--------|-----------|--------|--------|--------|-----------|
| BartXsum  | Background+Top-k-sentences        |        |        |        |           |        |        |        |           |
|           | Top-k-sentences                   |        |        |        |           |        |        |        |           |
|           | Sum_len+Top-k-sentences           |        |        |        |           |        |        |        |           |
|           | Sum_len+Background+Top-k-sentences|        |        |        |           |        |        |        |           |




# New Table

| Model      | Input Variant                         | Validation                            | Testing                                  |
|------------|---------------------------------------|---------------------------------------|------------------------------------------|
|            |                                       | Rouge1  | Rouge2 | RougeL | BERTScore | Rouge1  | Rouge2 | RougeL | BERTScore   |
|------------|---------------------------------------|---------|--------|--------|-----------|---------|--------|--------|-------------|
| BARTbase   | Background+Top-k-sentences            | 0.3021  | 0.0971 | 0.2077 | 0.86940   | 0.2750  | 0.10355 | 0.21127 | 0.8741    |
|            | Top-k-sentences                       | -       | -      | -      | -         | -       | -      | -      | -           |
|            | Sum_len+Top-k-sentences               | -       | -      | -      | -         | -       | -      | -      | -           |
|            | Sum_len+Background+Top-k-sentences    | -       | -      | -      | -         | -       | -      | -      | -           |
|------------|---------------------------------------|---------|--------|--------|-----------|---------|--------|--------|-------------|
| BartLarge  | Background+Top-k-sentences            | 0.3012  | 0.0937 | 0.2077 | 0.8682    | 0.2822  | 0.0956 | 0.2087 | 0.8716      |
|            | Top-k-sentences                       | -       | -      | -      | -         | -       | -      | -      | -           |
|            | Sum_len+Top-k-sentences               | -       | -      | -      | -         | -       | -      | -      | -           |
|            | Sum_len+Background+Top-k-sentences    | -       | -      | -      | -         | -       | -      | -      | -           |
|------------|---------------------------------------|---------|--------|--------|-----------|---------|--------|--------|-------------|
| BartCNN    | Background+Top-k-sentences            | 0.3101  | 0.1027 | 0.2129 | 0.8711    | 0.3320  | 0.1084 | 0.2166 | 0.8689      |
|            | Top-k-sentences                       | -       | -      | -      | -         | -       | -      | -      | -           |
|            | Sum_len+Top-k-sentences               | -       | -      | -      | -         | -       | -      | -      | -           |
|            | Sum_len+Background+Top-k-sentences    | -       | -      | -      | -         | -       | -      | -      | -           |
|------------|---------------------------------------|---------|--------|--------|-----------|---------|--------|--------|-------------|
| BartXsum   | Background+Top-k-sentences            | 0.3054  | 0.1004 | 0.2111 | 0.8697    | 0.2889  | 0.1007 | 0.2130 | 0.8727      |
|            | Top-k-sentences                       | -       | -      | -      | -         | -       | -      | -      | -           |
|            | Sum_len+Top-k-sentences               | -       | -      | -      | -         | -       | -      | -      | -           |
|            | Sum_len+Background+Top-k-sentences    | -       | -      | -      | -         | -       | -      | -      | -           |








