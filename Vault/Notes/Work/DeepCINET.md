2022-08-02@13:12

Status: #idea

Tags:

# DeepCINET

We have developed DeepCINET, a deep neural network used to rank pairs of samples based on genomic profiles. DeepCINET is inspired by Siamese networks composed of two identical “sister” neural nets, and the network trains on valid cell line pairs to…. A _valid_ cell line pair has a minimum AUC difference value, delta, between pairs to avoid noisy data.

DeepCINET is a deep neural network used to rank samples based on their genomic profiles. The architecture is inspired by Siamese neural networks composed of two identical "sister" neural nets, where a constrastive loss function is used to learn feature weights which maximally discriminate relative drug response between valid pairs of cancer cell-lines. A hyper-parameter, delta, is used to define what a valid pair is by setting a minimum difference in drug response (AUC) for pairs to be included in model training, with the intuition that useful weights cannot be learned from samples which are too close together in response-space.


---
# References
1. 