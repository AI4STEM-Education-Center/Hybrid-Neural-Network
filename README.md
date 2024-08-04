# Automatic Scoring of Students’ Science Writing Using Hybrid Neural Network

## Overview

This repository contains the implementation of a Hybrid Neural Network (HNN) for the automatic scoring of students' science writing. The approach is based on the paper titled "Automatic Scoring of Students’ Science Writing Using Hybrid Neural Network" presented at the AAAI2024 Workshop on AI for Education.

## Paper Title
**Automatic Scoring of Students’ Science Writing Using Hybrid Neural Network**

## Abstract

This study explores the efficacy of a multi-perspective hybrid neural network (HNN) for scoring student responses in science education with an analytic rubric. We compared the accuracy of the HNN model with four ML approaches (BERT, ANN, Naive Bayes, and Logistic Regression). The results have shown that HNN achieved 8%, 3%, 1%, and 0.12% higher accuracy than Naive Bayes, Logistic Regression, ANN, and BERT, respectively, for five scoring aspects (p < 0.001). The overall HNN’s perceived accuracy (M = 96.23%, SD = 1.45%) is comparable to the (training and inference) expensive BERT model’s accuracy (M = 96.12%, SD = 1.52%). We also have observed that HNN is twice as efficient in terms of training and inference compared to BERT and has comparable efficiency to the lightweight but less accurate Naive Bayes model. Our study confirmed the accuracy and efficiency of using HNN for automatically scoring students’ science writing.

## Approach

### Methodology

This study assessed middle school students' ability to use energy to explain scientific phenomena. The task employed in this study aligns with the Next Generation Science Standards (NGSS) performance expectations at the middle school level.

#### Participants
More than 1000 students from grades 6-8 participated in this study.

#### Assessment Item and Human Scoring
One assessment task was selected from the Next Generation Science Assessment, focusing on the application of chemistry ideas in real-world situations. A scoring rubric containing five response perspectives was developed, associated with each scoring aspect based on the dimensions of science learning.

#### Multi-Perspective HNN for Automatic Scoring
The HNN involves BERT for word embeddings, a Bi-LSTM layer for sequential processing, and an attention mechanism for weighting the importance of different input parts.

### Figures and Tables

#### Figure 1: Assessment Item

![Assessment Item](figures/assessment_item)

#### Figure 2: Hybrid Neural Network Architecture

![Hybrid Neural Network Architecture](figures/HNN_Architechture.pdf)

#### Table 1: Scoring Accuracy of Different Models

| Scoring Aspect | HNN (%) | ANN (%) | BERT (%) | Naive Bayes (NB) (%) | Logistic Regression (%) |
|----------------|---------|---------|----------|----------------------|-------------------------|
| 1              | 97.6    | 95.23   | 95.98    | 80.16                | 92.4                    |
| 2              | 98.1    | 93.14   | 96.77    | 85.48                | 91.93                   |
| 3              | 94.8    | 94.6    | 95.54    | 86.63                | 93.93                   |
| 4              | 97.4    | 96.82   | 95.54    | 95.54                | 95.14                   |
| 5              | 96.8    | 96.07   | 96.76    | 96.76                | 95.55                   |

#### Table 2: Scoring Rubric for Item “Gas-filled Balloons”

| Scoring Aspect | Perspectives | Elements                                                                 |
|----------------|--------------|--------------------------------------------------------------------------|
| 1              | SEP+DCI      | Student states that Gas A and D could be the same substance.             |
| 2              | SEP+CCC      | Student describes the pattern in the flammability data of Gas A and D.  |
| 3              | SEP+CCC      | Student describes the pattern in the density data of Gas A and D.       |
| 4              | DCI          | Student indicates flammability as a characteristic of identifying substances. |
| 5              | DCI          | Student indicates density as a characteristic of identifying substances.      |

### Results

Scoring accuracies for the five algorithms on the five scoring aspects are presented in Table 1. Except for Naive Bayes, all five algorithms yielded average scoring accuracy for the five aspects higher than .90. The HNN demonstrated significant accuracy improvements over other models, highlighting its potential for educational assessments.

### Training and Inference Efficiency

The training and inference efficiency of the multi-perspective HNN was compared to individual-perspective scoring algorithms. The HNN showed a significant reduction in inferencing time compared to BERT while maintaining high accuracy, making it a practical choice for real-time scoring applications.

## Conclusion

The multi-perspective HNN approach provides an effective solution for scoring complex constructs in science education. The results of this study demonstrate its superior accuracy and efficiency compared to traditional ML models, contributing to the development of more effective tools for educational assessment.

## Acknowledgments

This study is supported by the National Science Foundation (grants numbers 2101104, 2100964, 2101166, & 2101112). The authors are grateful for the PASTA team members. Any opinions, findings, conclusions, or recommendations expressed in this material are those of the author(s) and do not necessarily reflect the views of the NSF.

## References

A full list of references is available in the paper. For further reading and in-depth understanding, please refer to the paper "Automatic Scoring of Students’ Science Writing Using Hybrid Neural Network".

## Citation

If you use this model or code in your research, please cite our paper:
```
@article{latif2023automatic,
  title={Automatic Scoring of Students' Science Writing Using Hybrid Neural Network},
  author={Latif, Ehsan and Zhai, Xiaoming},
  journal={arXiv preprint arXiv:2312.03752},
  year={2023}
}
```

---

This README provides a comprehensive overview of the repository, including the abstract, approach, key figures, tables, and conclusions drawn from the research. For implementation details, refer to the code and documentation within the repository.

