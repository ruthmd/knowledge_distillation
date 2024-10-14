# Experiments related to knowledge distillation

#### Original Paper: [Distilling the Knowledge in a Neural Network](https://arxiv.org/abs/1503.02531)

#### Base Code: [PyTorch Knowledge Distillation Tutorial](https://pytorch.org/tutorials/beginner/knowledge_distillation_tutorial.html)

#### Dataset: CIFAR-10

## Accuracy by varying Temperature

| Temperature (T)   | Teacher accuracy (%) | Student accuracy without teacher (%) | Student accuracy with XE + KD (%) | Student accuracy with XE + CosineLoss (%) | Student accuracy with XE + RegressorMSE (%) |
|------|----------------------|--------------------------------------|-----------------------------------|--------------------------------------------|----------------------------------------------|
| 0.5  | 75.49                | 70.31                                | 70.33                             | 70.78                                      | 70.94                                        |
| 2.0  | 75.49                | 70.31                                | 70.71                             | 70.48                                      | 71.20                                        |
| 5.0  | 75.49                | 70.31                                | 72.18                             | 70.55                                      | 71.08                                        |
| 10.0 | 75.49                | 70.31                                | 72.07                             | 70.25                                      | 71.08                                        |
| 15.0 | 75.49                | 70.31                                | 71.35                             | 70.50                                      | 70.90                                        |
| 25.0 | 75.49                | 70.31                                | 71.36                             | 70.59                                      | 70.52                                        |

## Accuracy by varying Weight initialization methods 
| Initialization Method | KD    | Cosine | MSE   |
|-----------------------|-------|--------|-------|
| Default               | 71.82 | 69.84  | 69.74 |
| Xavier                | 70.85 | 70.50  | 69.50 |
| Kaiming               | 66.23 | 67.01  | 65.12 |
| Orthogonal            | 70.54 | 70.21  | 69.78 |
| Teacher               | 70.08 | 69.83  | 69.40 |
