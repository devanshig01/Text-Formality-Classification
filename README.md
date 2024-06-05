# Text-Formality-Classification

This project is based from the following paper: https://arxiv.org/pdf/2204.08975. This paper by Dementieva et al. (2023), discuses and evaluates various methods to detect formality across text in different languages. The paper utilizes various transformer based and BERT-based models and report the findings of which models have the highest accuracy in detecting text formality. 

Taking this paper a step further, we aimed to improve contextual understanding by developing a formality score scale of 0 to 1 and making further accurate sentence predictions. 

## Models Investigated and F1 scores:
- BiLSTM (Baseline model): 77.9%
- DeBerta: 93.7%
- Bert (uncased): 88.4%
- Simple CNN: 79.9%


Since DeBerta has the highest f1 score, we use that trained model to develop formality scores. Here are some examples:

<img width="1076" alt="Screenshot 2024-06-05 at 9 38 07 AM" src="https://github.com/devanshig01/Text-Formality-Classification/assets/68164303/81fc553c-d852-426e-8e86-9c3d5b2e2721">

